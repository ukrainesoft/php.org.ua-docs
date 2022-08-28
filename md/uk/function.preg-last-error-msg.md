Повертає повідомлення про помилку останньої запущеної функції PCRE

-   [« preg\_grep](function.preg-grep.html)
    
-   [preg\_last\_error »](function.preg-last-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCRE](ref.pcre.html)
    
-   Повертає повідомлення про помилку останньої запущеної функції PCRE
    

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

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() !== PREG_NO_ERROR) {
    echo preg_last_error_msg();
}

?>
```

Результат виконання цього прикладу:

```
Backtrack limit exhausted
```

### Дивіться також

-   [preg\_last\_error()](function.preg-last-error.html) - Повертає код помилки виконання останнього регулярного вираження PCRE