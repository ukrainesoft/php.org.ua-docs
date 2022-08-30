Повідомляє, чи токен ігноруватиметься парсером PHP

-   [« PhpToken::is](phptoken.is.md)
    
-   [PhpToken::toString »](phptoken.tostring.md)
    
-   [PHP Manual](index.md)
    
-   [PhpToken](class.phptoken.md)
    
-   Повідомляє, чи токен ігноруватиметься парсером PHP
    

# PhpToken::isIgnorable

(PHP 8)

PhpToken::isIgnorable — Повідомляє, чи буде токен ігноруватися парсером PHP

### Опис

```methodsynopsis
public PhpToken::isIgnorable(): bool
```

Повідомляє, чи токен ігноруватиметься парсером PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо токен ігноруватиметься парсером PHP (такі як пробільні послідовності або коментарі), то поверне **`true`**. В іншому випадку поверне **`false`**

### Приклади

**Приклад #1 Приклад використання **PhpToken::isIgnorable()****

```php
<?php
$echo = new PhpToken(T_ECHO, 'echo');
var_dump($echo->isIgnorable());   // -> bool(false)

$space = new PhpToken(T_WHITESPACE, ' ');
var_dump($space->isIgnorable());  // -> bool(true)
```

### Дивіться також

-   [PhpToken::tokenize()](phptoken.tokenize.md) - Розбирає заданий рядок, що містить програму на PHP, на масив об'єктів PhpToken