---
navigation:
  - function.preg-grep.md: « preg\_grep
  - function.preg-last-error.md: preg\_last\_error »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_last\_error\_msg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_last\_error\_msg

(PHP 8)

preg\_last\_error\_msg — Повертає повідомлення про помилку останньої запущеної функції PCRE

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

**Приклад #1 Приклад використання** preg\_last\_error\_msg()\*\*\*\*

```php
<?php

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() !== PREG_NO_ERROR) {
    echo preg_last_error_msg();
}

?>
```

Результат виконання наведеного прикладу:

```
Backtrack limit exhausted
```

### Дивіться також

-   [preg\_last\_error()](function.preg-last-error.md) \- Повертає код помилки виконання останнього регулярного вираження PCRE
