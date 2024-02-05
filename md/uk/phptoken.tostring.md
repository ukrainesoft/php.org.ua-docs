---
navigation:
  - phptoken.isignorable.md: '« PhpToken::isIgnorable'
  - phptoken.tokenize.md: 'PhpToken::tokenize »'
  - index.md: PHP Manual
  - class.phptoken.md: PhpToken
title: 'PhpToken::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PhpToken::\_\_function toString() { \[native code\] }

(PHP 8)

PhpToken::\_\_toString — Повертає текстовий вміст токена

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

**Приклад #1 Приклад використання** PhpToken::\_\_toString()\*\*\*\*

```php
<?php
$token = new PhpToken(T_ECHO, 'echo');
echo $token;
```

Результат виконання наведених прикладів:

```
echo
```

### Дивіться також

-   [token\_name()](function.token-name.md) \- Отримати символьне ім'я для переданої PHP-лексеми
