Повертає текстовий вміст токена

-   [« PhpToken::isIgnorable](phptoken.isignorable.html)
    
-   [PhpToken::tokenize »](phptoken.tokenize.html)
    
-   [PHP Manual](index.html)
    
-   [PhpToken](class.phptoken.html)
    
-   Повертає текстовий вміст токена
    

# PhpToken::function toString() { \[native code\] }

(PHP 8)

PhpToken::toString — Повертає текстовий вміст токена

### Опис

```methodsynopsis
public PhpToken::__toString(): string
```

Повертає текстовий вміст токена.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текстовий вміст токена.

### Приклади

**Приклад #1 Приклад використання **PhpToken::toString()****

```php
<?php
$token = new PhpToken(T_ECHO, 'echo');
echo $token;
```

Результат виконання даних прикладів:

```
echo
```

### Дивіться також

-   [token\_name()](function.token-name.html) - Отримати символьне ім'я для переданої PHP-лексеми