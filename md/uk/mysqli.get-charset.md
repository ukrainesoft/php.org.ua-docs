---
navigation:
  - mysqli.field-count.md: '« mysqli::$fieldcount'
  - mysqli.get-client-info.md: 'mysqli::$clientinfo »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::getcharset'
---
# mysqli::getcharset

# mysqligetcharset

(PHP 5> = 5.1.0, PHP 7, PHP 8)

mysqli::getcharset - mysqligetcharset — Повертає об'єкт, що описує кодування

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

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

**Приклад #1 Приклад використання **mysqli::getcharset()****

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

Результат виконання даних прикладів:

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

-   [mysqlicharactersetname()](mysqli.character-set-name.md) - Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqlisetcharset()](mysqli.set-charset.md) - Встановлює набір символів
