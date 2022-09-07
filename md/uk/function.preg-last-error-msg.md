---
navigation:
  - function.preg-grep.md: « preggrep
  - function.preg-last-error.md: preglasterror »
  - index.md: PHP Manual
  - ref.pcre.md: Функции PCRE
title: preglasterrormsg
---
# preglasterrormsg

(PHP 8)

preglasterrormsg — Повертає повідомлення про помилку останньої запущеної функції PCRE

### Опис

```methodsynopsis
preg_last_error_msg(): string
```

Повертає повідомлення про помилку останньої запущеної функції PCRE.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає повідомлення про помилку. Якщо помилок не було, повертає рядок `"No error"`

### Приклади

**Приклад #1 Приклад використання **preglasterrormsg()****

```php
<?php

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() !== PREG_NO_ERROR) {
    echo preg_last_error_msg();
}

?>
```

Результат виконання цього прикладу:

```
Backtrack limit exhausted
```

### Дивіться також

-   [preglasterror()](function.preg-last-error.md) - Повертає код помилки виконання останнього регулярного вираження PCRE
