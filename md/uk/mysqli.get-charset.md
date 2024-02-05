---
navigation:
  - mysqli.field-count.md: '« mysqli::$field\_count'
  - mysqli.get-client-info.md: 'mysqli::$client\_info »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::get\_charset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::get\_charset

# mysqli\_get\_charset

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

mysqli::get\_charset -- mysqli\_get\_charset — Повертає об'єкт, що описує кодування

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::get_charset(): ?object
```

Процедурний стиль

```methodsynopsis
mysqli_get_charset(mysqli $mysql): ?object
```

Повертає об'єкт, який містить властивості поточного кодування.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Функція повертає об'єкт із такими властивостями:

`charset`

Ім'я кодування

`collation`

Ім'я зіставлення

`dir`

Директорія, з якої отримано опис кодування. (?) або "" для вбудованих наборів

`min_length`

Мінімальна довжина символу в байтах

`max_length`

Максимальна довжина символу в байтах

`number`

Внутрішній номер кодування

`state`

Стан набору символів (?)

### Приклади

**Приклад #1 Приклад використання** mysqli::get\_charset()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
  $db = mysqli_init();
  $db->real_connect("localhost","root","","test");
  var_dump($db->get_charset());
?>
```

Процедурний стиль

```php
<?php
  $db = mysqli_init();
  mysqli_real_connect($db, "localhost","root","","test");
  var_dump(mysqli_get_charset($db));
?>
```

Результат виконання наведених прикладів:

```
object(stdClass)#2 (7) {
  ["charset"]=>
  string(6) "latin1"
  ["collation"]=>
  string(17) "latin1_swedish_ci"
  ["dir"]=>
  string(0) ""
  ["min_length"]=>
  int(1)
  ["max_length"]=>
  int(1)
  ["number"]=>
  int(8)
  ["state"]=>
  int(801)
}
```

### Дивіться також

-   [mysqli\_character\_set\_name()](mysqli.character-set-name.md) \- Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli\_set\_charset()](mysqli.set-charset.md) \- Встановлює набір символів
