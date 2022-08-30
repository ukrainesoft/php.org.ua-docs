Повертає ім'я токена

-   [« PhpToken::construct](phptoken.construct.html)
    
-   [PhpToken::is »](phptoken.is.html)
    
-   [PHP Manual](index.html)
    
-   [PhpToken](class.phptoken.html)
    
-   Повертає ім'я токена
    

# PhpToken::getTokenName

(PHP 8)

PhpToken::getTokenName — Повертає ім'я токена

### Опис

```methodsynopsis
public PhpToken::getTokenName(): ?string
```

Повертає ім'я токена.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Символ ASCII для односимвольних токенів, або ім'я однієї з констант T (дивіться [Список меток (tokens) парсера](tokens.html)), або \*\*`null`\*\*для невідомих токенів.

### Приклади

**Приклад #1 Приклад використання **PhpToken::getTokenName()****

```php
<?php
// стандартный токен
$token = new PhpToken(T_ECHO, 'echo');
var_dump($token->getTokenName());   // -> string(6) "T_ECHO"

// односимвольный токен
$token = new PhpToken(ord(';'), ';');
var_dump($token->getTokenName());   // -> string(1) ";"

// неизвестный токен
$token = new PhpToken(10000 , "\0");
var_dump($token->getTokenName());   // -> NULL
```

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.html) - Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken
-   [tokenname()](function.token-name.html) - Отримати символьне ім'я для переданої PHP-лексеми