---
navigation:
  - mongodb-driver-readconcern.unserialize.md: '« MongoDB\\Driver\\ReadConcern::unserialize'
  - mongodb-driver-cursor.construct.md: 'MongoDB\\Driver\\Cursor::\_\_construct »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDB\\Driver
title: Клас MongoDB\\Driver\\Cursor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас MongoDB\\Driver\\Cursor

(mongodb >=1.0.0)

## Вступ

Класс**MongoDB\\Driver\\Cursor** містить результати команди MongoDB command або запиту та може бути повернутий [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md) або [MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md)соответственно.

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\Cursor
     

     implements 
       MongoDB\Driver\CursorInterface,  Iterator {
    

    /* Методы */
    
   final private __construct()
public current(): array|object|null
final public getId(): MongoDB\Driver\CursorId
final public getServer(): MongoDB\Driver\Server
final public isDead(): bool
public key(): int
public next(): void
public rewind(): void
final public setTypeMap(array $typemap): void
final public toArray(): array
public valid(): bool

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.9.0 | Реалізує [Iterator](class.iterator.md) |
| PECL mongodb 1.6.0 | Реалізує [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.md), який успадковує [Traversable](class.traversable.md) |

## Приклади

**Приклад #1 Reading a result set**

Як [MongoDB\\Driver\\Manager::executeCommand()](mongodb-driver-manager.executecommand.md), так[MongoDB\\Driver\\Manager::executeQuery()](mongodb-driver-manager.executequery.md), повертають свої результати у вигляді об'єкту **MongoDB\\Driver\\Cursor**

Оскільки **MongoDB\\Driver\\Cursor** реалізує інтерфейс [Traversable](class.traversable.md), ви можете ітерувати за набором результату за допомогою [`foreach`](control-structures.foreach.md)

```php
<?php

$manager = new MongoDB\Driver\Manager();

/* Вставить определённые документы, чтобы наш запрос вернул результаты */
$bulkWrite = new MongoDB\Driver\BulkWrite;
$bulkWrite->insert(['name' => 'Ceres', 'size' => 946, 'distance' => 2.766]);
$bulkWrite->insert(['name' => 'Vesta', 'size' => 525, 'distance' => 2.362]);
$manager->executeBulkWrite("test.asteroids", $bulkWrite);

/* Запрос на получение всех элементов в коллекции */
$query = new MongoDB\Driver\Query( [] );

/* Запрос коллекции "asteroids" базы данных "test" */
$cursor = $manager->executeQuery("test.asteroids", $query);

/* Теперь $cursor содержит объект, обёрнутый вокруг набора с результатом. Используйте
 * foreach() для итеации по всему результату */
foreach ($cursor as $document) {
    print_r($document);
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
stdClass Object
(
    [_id] => MongoDB\BSON\ObjectId Object
        (
            [oid] => 5a4cff2f122d3321565d8cc2
        )

    [name] => Ceres
    [size] => 946
    [distance] => 2.766
)
stdClass Object
(
    [_id] => MongoDB\BSON\ObjectId Object
        (
            [oid] => 5a4cff2f122d3321565d8cc3
        )

    [name] => Vesta
    [size] => 525
    [distance] => 2.362
}
```

**Приклад #2 Читання результатів для хвостового курсору**

[» Хвостові курсори](https://www.mongodb.com/docs/manual/core/tailable-cursors) - - це особливий тип курсору MongoDB, який дозволяє клієнту читати деякі результати, а потім чекати, доки не з'являться додаткові документи. Ці курсори в основному використовуються з [» Capped Collections](https://www.mongodb.com/docs/manual/core/capped-collections) і [» Change Streams](https://www.mongodb.com/docs/manual/changeStreams)

Хоча звичайні курсори можна ітерувати один раз за допомогою `foreach`, цей підхід не працюватиме з хвостовими курсорами. Коли `foreach` використовується з хвостовим курсором, цикл зупиняється після досягнення кінця початкового набору результатів. Спроба продовжити ітерацію курсору з другим `foreach` викинути виняток, оскільки PHP намагається перемотати курсор. Подібно до об'єктів результатів в інших драйверах баз даних, курсори в MongoDB підтримують лише ітерацію вперед, що означає, що вони не можуть бути перемотані.

Для безперервного зчитування з хвостового курсору об'єкт курсора повинен бути загорнутий за допомогою [IteratorIterator](class.iteratoriterator.md). Це дозволяє застосуванню безпосередньо керувати ітерацією курсору, уникати ненавмисного перемотування курсору і вирішувати, коли чекати на нові результати або повністю припинити ітерацію.

Щоб продемонструвати хвостовий курсор у дії, будуть використовуватися два скрипти: "виробник" (producer) та "споживач" (consumer). Скрипт продюсера створить нову capped-колекцію, використовуючи команду [» create](https://www.mongodb.com/docs/manual/reference/command/create) і почне вставляти новий документ у цю колекцію кожну секунду.

```php
<?php

$manager = new MongoDB\Driver\Manager;

$manager->executeCommand('test', new MongoDB\Driver\Command([
    'create' => 'asteroids',
    'capped' => true,
    'size' => 1048576,
]));

while (true) {
    $bulkWrite = new MongoDB\Driver\BulkWrite;
    $bulkWrite->insert(['createdAt' => new MongoDB\BSON\UTCDateTime]);
    $manager->executeBulkWrite('test.asteroids', $bulkWrite);

    sleep(1);
}

?>
```

Коли скрипт продюсера (producer) все ще запущений, може бути виконаний другий скрипт для читання вставлених документів за допомогою хвостового (tailable) курсора, позначеного параметрами `tailable`и`awaitData`для[MongoDB\\Driver\\Query::\_\_construct()](mongodb-driver-query.construct.md)

```php
<?php

$manager = new MongoDB\Driver\Manager;

$query = new MongoDB\Driver\Query([], [
    'tailable' => true,
    'awaitData' => true,
]);

$cursor = $manager->executeQuery('test.asteroids', $query);

$iterator = new IteratorIterator($cursor);

$iterator->rewind();

while (true) {
    if ($iterator->valid()) {
        $document = $iterator->current();
        printf("Пользовательский документ создан: %s\n", $document->createdAt);
    }

    $iterator->next();
}

?>
```

Скрипт користувача почне з швидкого друку всіх доступних документів у заблокованій колекції (як би використовувався `foreach`); однак, при досягненні кінця початкового набору результатів він не завершиться. Оскільки курсор є хвостовим, виклик [IteratorIterator::valid()](iteratoriterator.valid.md) буде блокувати та чекати на додаткові результати . [IteratorIterator::valid()](iteratoriterator.valid.md) також використовується для перевірки наявності на кожному етапі даних, доступних для читання.

> **Зауваження**: У цьому прикладі використовується опція запиту `awaitData`, щоб проінструктувати сервер блокувати протягом короткого періоду (наприклад, одну секунду) наприкінці набору результатів перед поверненням відповіді драйверу. Це використовується для запобігання агресивному опитуванню (polling) серверу за відсутності результатів. Параметр `maxAwaitTimeMS` може використовуватися в поєднанні з `tailable`и`awaitData`, щоб вказати час, який сервер повинен блокувати, коли він досягне кінця набору результатів.

## Помилки

При ітерації об'єктом курсору дані BSON перетворюються на змінні PHP. Ця ітерація може викликати такі винятки:

-   Викидає [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)якщо клас на карті типів не може бути створений або не реалізує[MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.md)
-   Исключение[MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.md)викидається, якщо вхідні дані не є одним документом BSON. Можливі причини включають, але не обмежені некоректним BSON, зайвими даними або несподіваною помилкою[» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson)

## Зміст

-   [MongoDB\\Driver\\Cursor::\_\_construct](mongodb-driver-cursor.construct.md)— Створює новий об'єкт Cursor (не використовується)
-   [MongoDB\\Driver\\Cursor::current](mongodb-driver-cursor.current.md)— Повертає поточний елемент
-   [MongoDB\\Driver\\Cursor::getId](mongodb-driver-cursor.getid.md)— Повертає ідентифікатор для курсору
-   [MongoDB\\Driver\\Cursor::getServer](mongodb-driver-cursor.getserver.md)— Повертає сервер, пов'язаний із курсором
-   [MongoDB\\Driver\\Cursor::isDead](mongodb-driver-cursor.isdead.md)— Перевіряє, чи курсор вичерпано, чи може містити додаткові результати.
-   [MongoDB\\Driver\\Cursor::key](mongodb-driver-cursor.key.md)— Повертає індекс поточного результату у курсорі
-   [MongoDB\\Driver\\Cursor::next](mongodb-driver-cursor.next.md)— Переміщує курсор на наступний результат
-   [MongoDB\\Driver\\Cursor::rewind](mongodb-driver-cursor.rewind.md)— Переміщує курсор до першого результату
-   [MongoDB\\Driver\\Cursor::setTypeMap](mongodb-driver-cursor.settypemap.md)— Встановлює карту типу для десеріалізації BSON
-   [MongoDB\\Driver\\Cursor::toArray](mongodb-driver-cursor.toarray.md)— Повертає масив, що містить усі результати курсору
-   [MongoDB\\Driver\\Cursor::valid](mongodb-driver-cursor.valid.md)— Перевіряє, чи поточна позиція курсору коректна.
