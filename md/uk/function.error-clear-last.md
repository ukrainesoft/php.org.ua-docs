Очистити останню помилку

-   [« debugprintbacktrace](function.debug-print-backtrace.html)
    
-   [errorgetlast »](function.error-get-last.html)
    
-   [PHP Manual](index.html)
    
-   [Функции обработки ошибок](ref.errorfunc.html)
    
-   Очистити останню помилку
    

# errorclearlast

(PHP 7, PHP 8)

errorclearlast — Очистити останню помилку

### Опис

```methodsynopsis
error_clear_last(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Очищає останню помилку, унеможливлюючи отримання її за допомогою [errorgetlast()](function.error-get-last.html)

### Приклади

**Приклад #1 Приклад **errorclearlast()****

```php
<?php
var_dump(error_get_last());
error_clear_last();
var_dump(error_get_last());

@$a = $b;

var_dump(error_get_last());
error_clear_last();
var_dump(error_get_last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
NULL
NULL
array(4) {
  ["type"]=>
  int(8)
  ["message"]=>
  string(21) "Undefined variable: b"
  ["file"]=>
  string(9) "%s"
  ["line"]=>
  int(6)
}
NULL
```

### Дивіться також

-   [Константы ошибок](errorfunc.constants.html)