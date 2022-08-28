Повертає об'єкт, що описує кодування

-   [« mysqli::$field\_count](mysqli.field-count.html)
    
-   [mysqli::$client\_info »](mysqli.get-client-info.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Повертає об'єкт, що описує кодування
    

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

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
  $db = mysqli_init();
  $db->real_connect("localhost","root","","test");
  var_dump($db->get_charset());
?>
```

Процедурний стиль

```php
<?php
  $db = mysqli_init();
  mysqli_real_connect($db, "localhost","root","","test");
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

-   [mysqli\_character\_set\_name()](mysqli.character-set-name.html) - Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli\_set\_charset()](mysqli.set-charset.html) - Встановлює набір символів