---
navigation:
  - phptoken.isignorable.md: '« PhpToken::isIgnorable'
  - phptoken.tokenize.md: 'PhpToken::tokenize »'
  - index.md: PHP Manual
  - class.phptoken.md: PhpToken
title: 'PhpToken::function toString() { \[native code\] }'
---
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

-   [tokenname()](function.token-name.md) - Отримати символьне ім'я для переданої PHP-лексеми
