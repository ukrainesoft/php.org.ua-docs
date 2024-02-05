---
navigation:
  - changelog.mysql_xdevapi.md: '" Список змін'
  - ref.mysql-xdevapi.md: Функції Mysql\_xdevapi »
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

Центральна точка входу в X DevAPI – функція **mysql\_xdevapi\\getSession()**, яка приймає URI сервер MySQL 8.0 і повертає об'єкт **mysql\_xdevap\\Session**

**Приклад #1 Підключення до сервера MySQL**

```php
<?php
try {
    $session = mysql_xdevapi\getSession("mysqlx://user:password@host");
} catch(Exception $e) {
    die("Не удалось установить соединение: " . $e->getMessage());
}

// ... используйте $session
?>
```

Сесія надає повний доступ до API. Перший крок для нової установки MySQL-сервера - це створення схеми бази даних із колекцією для зберігання даних:

**Приклад #2 Створення схеми та колекції на сервері MySQL**

```php
<?php
$schema = $session->createSchema("test");
$collection = $schema->createCollection("example");
?>
```

При збереженні даних їх зазвичай кодують JSON-формат функцією [json\_encode()](function.json-encode.md), який може бути збережений всередині колекції.

У наступному прикладі дані зберігаються в колекції, яку ми створили раніше, а потім знову витягуємо їх частини.

**Приклад #3 Зберігання та отримання даних**

```php
<?php
$marco = [
  "name" => "Marco",
  "age"  => 19,
  "job"  => "Programmer"
];
$mike = [
  "name" => "Mike",
  "age"  => 39,
  "job"  => "Manager"
];

$schema = $session->getSchema("test");
$collection = $schema->getCollection("example");

$collection->add($marco, $mike)->execute();

var_dump($collection->find("name = 'Mike'")->execute()->fetchOne());
?>
```

Висновок наведеного прикладу буде схожим на:

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

У прикладі показано, що MySQL сервер додає поле з ім'ям `_id`що виступає в ролі первинного ключа до документа.

У прикладі також показано, що вилучені дані відсортовані за абеткою. Цей конкретний порядок обґрунтований ефективним двійковим сховищем усередині сервера MySQL, але на нього не потрібно покладатися. Докладніше про це розказано в документації типу даних MySQL JSON.

За бажанням можна використовувати ітератори PHP для вилучення кількох документів:

**Приклад #4 Вилучення та ітерація кількох документів**

```php
<?php
$result = $collection->find()->execute();
foreach ($result as $doc) {
  echo "${doc["name"]} is a ${doc["job"]}.\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Marco is a Programmer.
Mike is a Manager.
```
