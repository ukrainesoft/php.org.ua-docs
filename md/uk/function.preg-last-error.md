---
navigation:
  - function.preg-last-error-msg.md: « preg\_last\_error\_msg
  - function.preg-match-all.md: preg\_match\_all »
  - index.md: PHP Manual
  - ref.pcre.md: Функції PCRE
title: preg\_last\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# preg\_last\_error

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

preg\_last\_error — Повертає код помилки виконання останнього регулярного виразу PCRE

### Опис

```methodsynopsis
preg_last_error(): int
```

Повертає код помилки виконання останнього регулярного виразу PCRE.

**Приклад #1 Приклад використання** preg\_last\_error()\*\*\*\*

```php
<?php

preg_match('/(?:\D+|<\d+>)*[!?]/', 'foobar foobar foobar');

if (preg_last_error() == PREG_BACKTRACK_LIMIT_ERROR) {
    echo 'Был исчерпан лимит обратных ссылок!';
}

?>
```

Результат виконання наведеного прикладу:

```
Был исчерпан лимит обратных ссылок!
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає одну з наступних констант ([описаних на окремій сторінці.](pcre.constants.md)):

-   **`PREG_NO_ERROR`**
-   **`PREG_INTERNAL_ERROR`**
-   **`PREG_BACKTRACK_LIMIT_ERROR`**(смотрите также[pcre.backtrack\_limit](pcre.configuration.md#ini.pcre.backtrack-limit)) .
-   **`PREG_RECURSION_LIMIT_ERROR`**(смотрите также[pcre.recursion\_limit](pcre.configuration.md#ini.pcre.recursion-limit)) .
-   **`PREG_BAD_UTF8_ERROR`**
-   **`PREG_BAD_UTF8_OFFSET_ERROR`**
-   **`PREG_JIT_STACKLIMIT_ERROR`**

### Дивіться також

-   [preg\_last\_error\_msg()](function.preg-last-error-msg.md) \- Повертає повідомлення про помилку останньої запущеної функції PCRE
