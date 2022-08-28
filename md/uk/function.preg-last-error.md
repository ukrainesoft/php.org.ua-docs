Повертає код помилки виконання останнього регулярного виразу PCRE

-   [« preg\_last\_error\_msg](function.preg-last-error-msg.html)
    
-   [preg\_match\_all »](function.preg-match-all.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PCRE](ref.pcre.html)
    
-   Повертає код помилки виконання останнього регулярного виразу PCRE
    

# preglasterror

(PHP 5> = 5.2.0, PHP 7, PHP 8)

preglasterror — Повертає код помилки виконання останнього регулярного виразу PCRE

### Опис

```methodsynopsis
preg_last_error(): int
```

Повертає код помилки виконання останнього регулярного виразу PCRE.

**Приклад #1 Приклад використання **preglasterror()****

```php
<?php

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() == PREG_BACKTRACK_LIMIT_ERROR) {
    echo 'Был исчерпан лимит обратных ссылок!';
}

?>
```

Результат виконання цього прикладу:

```
Был исчерпан лимит обратных ссылок!
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає одну з наступних констант ([описанных на отдельной странице.](pcre.constants.html)

-   **`PREG_NO_ERROR`**
-   **`PREG_INTERNAL_ERROR`**
-   **`PREG_BACKTRACK_LIMIT_ERROR`** (Дивіться також [pcre.backtrack\_limit](pcre.configuration.html#ini.pcre.backtrack-limit)
-   **`PREG_RECURSION_LIMIT_ERROR`** (Дивіться також [pcre.recursion\_limit](pcre.configuration.html#ini.pcre.recursion-limit)
-   **`PREG_BAD_UTF8_ERROR`**
-   **`PREG_BAD_UTF8_OFFSET_ERROR`**
-   **`PREG_JIT_STACKLIMIT_ERROR`**

### Дивіться також

-   [preg\_last\_error\_msg()](function.preg-last-error-msg.html) - Повертає повідомлення про помилку останньої запущеної функції PCRE