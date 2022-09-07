---
navigation:
  - function.debug-print-backtrace.md: « debugprintbacktrace
  - function.error-get-last.md: errorgetlast »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: errorclearlast
---
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

Очищає останню помилку, унеможливлюючи отримання її за допомогою [errorgetlast()](function.error-get-last.md)

### Приклади

**Приклад #1 Приклад **errorclearlast()****

```php
<?php
var_dump(error_get_last());
error_clear_last();
var_dump(error_get_last());

@$a = $b;

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

-   [Константи помилок](errorfunc.constants.md)
