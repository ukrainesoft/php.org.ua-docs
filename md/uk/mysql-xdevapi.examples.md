---
navigation:
  - changelog.mysql_xdevapi.md: « Список изменений
  - ref.mysql-xdevapi.md: Функції Mysqlxdevapi »
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Приклади
---
# Приклади

Центральною точкою входу в X DevAPI є функція \*\*mysqlxdevapigetSession()\*\*яка отримує URI на сервер MySQL 8.0 і повертає об'єкт **mysqlxdevapSession**

**Приклад #1 Підключення до сервера MySQL**

```php
<?php
try {
    $session = mysql_xdevapi\getSession("mysqlx://user:password@host");
} catch(Exception $e) {
    die("Не удалось установить соединение: " . $e->getMessage());
}

// ... используйте $session
?>
```

Сесія забезпечує повний доступ до API. Для нової установки сервера MySQL першим кроком є ​​створення схеми бази даних із колекцією для зберігання даних:

**Приклад #2 Створення схеми та колекції на сервері MySQL**

```php
<?php
$schema = $session->createSchema("test");
$collection = $schema->createCollection("example");
?>
```

При зберіганні даних, як правило, [jsonencode()](function.json-encode.md) використовується для кодування даних JSON, який потім може зберігатися в колекції.

У наступному прикладі дані зберігаються в колекції, яку ми створили раніше, а потім знову витягуємо їх частини.

**Приклад #3 Зберігання та отримання даних**

```php
<?php
$marco = [
  "name" => "Marco",
  "age"  => 19,
  "job"  => "Programmer"
];
$mike = [
  "name" => "Mike",
  "age"  => 39,
  "job"  => "Manager"
];

$schema = $session->getSchema("test");
$collection = $schema->getCollection("example");

$collection->add($marco, $mike)->execute();

var_dump($collection->find("name = 'Mike'")->execute()->fetchOne());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(4) {
  ["_id"]=>
  string(28) "00005ad66aaf0000000000000003"
  ["age"]=>
  int(39)
  ["job"]=>
  string(7) "Manager"
  ["name"]=>
  string(4) "Mike"
}
```

Приклад показує, що сервер MySQL додає додаткове поле з ім'ям `_id`, що є первинним ключем до документа.

У прикладі також показано, що вилучені дані сортуються за абеткою. Цей конкретний порядок виходить з ефективного двійкового сховища всередині сервера MySQL, але не слід покладатися на нього. За подробицями зверніться до документації типу даних MySQL JSON.

За бажанням можна використовувати ітератори PHP для вилучення кількох документів:

**Приклад #4 Вилучення та ітерація кількох документів**

```php
<?php
$result = $collection->find()->execute();
foreach ($result as $doc) {
  echo "${doc["name"]} is a ${doc["job"]}.\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Marco is a Programmer.
Mike is a Manager.
```
