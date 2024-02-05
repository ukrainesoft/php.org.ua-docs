---
navigation:
  - mongodb-driver-monitoring-commandsubscriber.commandsucceeded.md: '« MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded'
  - mongodb-driver-monitoring-logsubscriber.log.md: 'MongoDB\\Driver\\Monitoring\\LogSubscriber::log »'
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Інтерфейс MongoDB\\Driver\\Monitoring\\LogSubscriber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\Driver\\Monitoring\\LogSubscriber

(mongodb >=1.17.0)

## Вступ

Класам, які реалізують цей інтерфейс, дозволено реєструватися як передплатники та отримувати повідомлення журналу від драйвера. Це схоже на ведення журналу налагодження на основі потоків (тобто директива [mongodb.debug](mongodb.configuration.md#ini.mongodb.debug)), за винятком того, що повідомлення журналу рівня трасування не приймаються.

Як і у випадку з потоковим журналуванням, глобально зареєструвати логер можна лише методом [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md). Драйвер не може розрізняти повідомлення журналу для окремих об'єктів. [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.md)

## Огляд інтерфейсів

```classsynopsis



    
     
      class MongoDB\Driver\Monitoring\LogSubscriber
     

     implements 
       MongoDB\Driver\Monitoring\Subscriber {


    /* Константы */
    
     const
     int
      LEVEL_ERROR = 0;

    const
     int
      LEVEL_CRITICAL = 1;

    const
     int
      LEVEL_WARNING = 2;

    const
     int
      LEVEL_MESSAGE = 3;

    const
     int
      LEVEL_INFO = 4;

    const
     int
      LEVEL_DEBUG = 5;


    /* Методы */
    
   abstract public log(int $level, string $domain, string $message): void

   }
```

## Обумовлені константи

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_ERROR`**

Рівень журналу помилок. Стан помилки, про який драйвер не в змозі повідомити через API. Це найсерйозніший рівень журналу у драйвері.

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_CRITICAL`**

Критичний рівень журналу. Стан помилки з дещо меншою серйозністю. Ця константа існує для узгодженості з модулем libmongoc, однак драйвер навряд чи буде використовувати його на практиці.

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_WARNING`**

Рівень журналу попереджень. Вказує на ситуацію, за якої є ризик небажаної поведінки програми.

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_MESSAGE`**

Рівень журналу повідомлень або повідомлень. Вказує на незвичайну, але не проблематичну подію.

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_INFO`**

Інформаційний рівень журналу. Інформація високого рівня нормальної поведінки драйвера.

**`MongoDB\Driver\Monitoring\LogSubscriber::LEVEL_DEBUG`**

Рівень журналу налагодження. Детальна інформація, корисна при налагодженні програми.

## Зміст

-   [MongoDB\\Driver\\Monitoring\\LogSubscriber::log](mongodb-driver-monitoring-logsubscriber.log.md)— Метод сповіщення для повідомлення журналу
