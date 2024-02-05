---
navigation:
  - function.debug-print-backtrace.md: « debug\_print\_backtrace
  - function.error-get-last.md: error\_get\_last »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: error\_clear\_last
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# error\_clear\_last

(PHP 7, PHP 8)

error\_clear\_last — Очистити останню помилку

### Опис

```methodsynopsis
error_clear_last(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Очищає останню помилку, унеможливлюючи отримання її за допомогою [error\_get\_last()](function.error-get-last.md)

### Приклади

**Пример #1 Пример**error\_clear\_last()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

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
