---
navigation:
  - mongodb.tutorial.library.md: « Использование библиотеки PHP для MongoDB (PHPLIB)
  - mongodb.architecture.md: Архитектура и внутреннее устройство драйвера »
  - index.md: PHP Manual
  - mongodb.tutorial.md: Навчальні матеріали
title: >-
  Моніторинг продуктивності програми (Application Performance Monitoring або
  APM)
---
# Моніторинг продуктивності програми (Application Performance Monitoring або APM)

Драйвер MongoDB містить API передплатника подій, який дозволяє програмам відстежувати команди та внутрішню активність, що відноситься до [» Спецификации обнаружения и мониторинга серверов](https://github.com/mongodb/specifications/blob/master/source/server-discovery-and-monitoring/server-discovery-and-monitoring.rst). У цьому посібнику буде продемонстровано моніторинг команд за допомогою інтерфейсу [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md)

Інтерфейс [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.md) визначає три методи: `commandStarted` `commandSucceeded` і `commandFailed`. Кожен із них приймає один параметр `event` класу, що відповідає потрібній події. Наприклад, `commandSucceeded` приймає аргумент `$event` класу [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.md)

У цьому посібнику ви реалізуємо передплатника, який створює список профілювань усіх запитів та середнього часу їх виконання.

## Клас передплатник Scaffolding

Ми почнемо з шаблону для нашого передплатника:

```php
<?php

class QueryTimeCollector implements \MongoDB\Driver\Monitoring\CommandSubscriber
{
    public function commandStarted( \MongoDB\Driver\Monitoring\CommandStartedEvent $event ): void
    {
    }

    public function commandSucceeded( \MongoDB\Driver\Monitoring\CommandSucceededEvent $event ): void
    {
    }

    public function commandFailed( \MongoDB\Driver\Monitoring\CommandFailedEvent $event ): void
    {
    }
}

?>
```

## Реєстрація передплатника

Як тільки об'єкт передплатник створено, необхідно його зареєструвати в драйвері системи моніторингу. Реєстрація здійснюється методом [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) або [MongoDBDriverManager::addSubscriber()](mongodb-driver-manager.addsubscriber.md) для реєстрації передплатника глобально або за допомогою певного класу Manager відповідно.

```php
<?php

\MongoDB\Driver\Monitoring\addSubscriber( new QueryTimeCollector() );

?>
```

## Реалізуємо логіку

Тепер займемося реалізацією логіки класу передплатника. Для порівняння двох подій, що належать до успішно виконаної команди (commandStarted and commandSucceeded), кожен об'єкт події надає поле `requestId`

Для запису середнього часу виконання запиту ми почнемо з відстеження команди `find` у події підтримуєтьсяпідпис. Ми будемо додавати елемент до масиву `pendingCommands` з індексом відповідним `requestId` та значенням, що відповідає запиту.

Коли ми отримаємо відповідну подію commandSucceeded з відповідним `requestId`, ми додамо час виконання (з `durationMicros`) до загального часу та збільшимо лічильник операцій.

Якщо ми отримаємо подію commandFailed, ми просто видалимо відповідний запис з `pendingCommands`

```php
<?php

class QueryTimeCollector implements \MongoDB\Driver\Monitoring\CommandSubscriber
{
    private $pendingCommands = [];
    private $queryShapeStats = [];

    /* Создаёт форму запроса из аргумента фильтра. В данный момент учитываются
     * только поля верхнего уровня. */
    private function createQueryShape( array $filter )
    {
        return json_encode( array_keys( $filter ) );
    }

    public function commandStarted( \MongoDB\Driver\Monitoring\CommandStartedEvent $event ): void
    {
        if ( array_key_exists( 'find', (array) $event->getCommand() ) )
        {
            $queryShape = $this->createQueryShape( (array) $event->getCommand()->filter );
            $this->pendingCommands[$event->getRequestId()] = $queryShape;
        }
    }

    public function commandSucceeded( \MongoDB\Driver\Monitoring\CommandSucceededEvent $event ): void
    {
        $requestId = $event->getRequestId();
        if ( array_key_exists( $requestId, $this->pendingCommands ) )
        {
            $this->queryShapeStats[$this->pendingCommands[$requestId]]['count']++;
            $this->queryShapeStats[$this->pendingCommands[$requestId]]['duration'] += $event->getDurationMicros();
            unset( $this->pendingCommands[$requestId] );
        }
    }

    public function commandFailed( \MongoDB\Driver\Monitoring\CommandFailedEvent $event ): void
    {
        if ( array_key_exists( $event->getRequestId(), $this->pendingCommands ) )
        {
            unset( $this->pendingCommands[$event->getRequestId()] );
        }
    }

    public function __destruct()
    {
        foreach( $this->queryShapeStats as $shape => $stats )
        {
            echo "Shape: ", $shape, " (", $stats['count'], ")\n  ",
                $stats['duration'] / $stats['count'], "µs\n\n";
        }
    }
}

$m = new \MongoDB\Driver\Manager( 'mongodb://localhost:27016' );

/* Добавляем подписчика */
\MongoDB\Driver\Monitoring\addSubscriber( new QueryTimeCollector() );

/* Запускаем пачку запросов */
$query = new \MongoDB\Driver\Query( [
    'region_slug' => 'scotland-highlands', 'age' => [ '$gte' => 20 ]
] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

$query = new \MongoDB\Driver\Query( [
    'region_slug' => 'scotland-lowlands', 'age' => [ '$gte' => 15 ]
] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

$query = new \MongoDB\Driver\Query( [ 'region_slug' => 'scotland-lowlands' ] );
$cursor = $m->executeQuery( 'dramio.whisky', $query );

?>
```
