---
navigation:
  - mongodb.security.request_injection.md: Атака за допомогою ін'єкцій у запиті
  - book.mongodb.md: MongoDB\\Driver »
  - index.md: PHP Manual
  - mongodb.security.md: Безпека
title: Атака за допомогою ін'єкцій у скриптах
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Атака за допомогою ін'єкцій у скриптах

Якщо ви використовуєте JavaScript, переконайтеся, що всі змінні, які перетинають кордон PHP-JavaScript, передаються в поле `scope` [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.md), а не інтерполуються у рядок JavaScript. Це може виникнути під час використання пропозицій `$where` у запитах, командах mapReduce та group, а також у будь-який інший час, коли ви можете передати JavaScript до бази даних.

Наприклад, припустимо, що ми маємо деякий JavaScript, щоб вітати користувача в журналах бази даних. Ми могли б зробити:

```php
<?php
$m = new MongoDB\Driver\Manager;

// Не делайте так!!!
$username = $_GET['field'];

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "print('Привет, $username!');"
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

Однак що, якщо зловмисник передасть JavaScript?

```php
<?php
$m = new MongoDB\Driver\Manager;

// Не делайте так!!!
$username = $_GET['field'];
// $username is set to "'); db.users.drop(); print('"

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "print('Привет, $username!');"
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

Тепер MongoDB виконає рядок JavaScript `"print('Привіт, '); db.users.drop(); print('!');"`. Цю атаку легко уникнути: використовуйте `args` для передачі змінних з PHP до JavaScript:

```php
<?php
$m = new MongoDB\Driver\Manager;

$_GET['field'] = 'derick';
$args = [ $_GET['field'] ];

$cmd = new \MongoDB\Driver\Command( [
    'eval' => "function greet(username) { print('Привет, ' + username + '!'); }",
    'args' => $args,
] );

$r = $m->executeCommand( 'dramio', $cmd );
?>
```

Це додає аргумент у область JavaScript, яка використовується як аргумент для функції `greet`. Тепер, якщо хтось спробує надіслати шкідливий код, MongoDB надрукує нешкідливо `Вітання, '); db.dropDatabase(); print('!`

Використання аргументів допомагає запобігти виконанню шкідливого введення базою даних. Тим не менш, ви повинні переконатися, що ваш код не перевернеться і все одно виконає введення! Найкраще уникати виконання *будь-якого*JavaScript на сервере.

Настійно рекомендується уникати речення [» $where clause](https://www.mongodb.com/docs/manual/reference/operator/query/where/#considerations) із запитами, оскільки це суттєво впливає на продуктивність. По можливості використовуйте або звичайні оператори запитів, або [» Aggregation Framework](https://www.mongodb.com/docs/manual/core/aggregation-pipeline)

Як альтернатива [» MapReduce](https://www.mongodb.com/docs/manual/core/map-reduce/), що використовує JavaScript, розгляньте можливість використання [» Aggregation Framework](https://www.mongodb.com/docs/manual/core/aggregation-pipeline). На відміну від Map/Reduce, він використовує ідіоматичний мову для побудови запитів, без необхідності писати та використовувати повільніший підхід JavaScript, який потрібний для Map/Reduce.

Команда[» eval](https://www.mongodb.com/docs/manual/reference/command/eval/) застаріла з MongoDB 3.0, і її слід уникати.
