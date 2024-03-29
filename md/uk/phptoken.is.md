---
navigation:
  - phptoken.gettokenname.md: '« PhpToken::getTokenName'
  - phptoken.isignorable.md: 'PhpToken::isIgnorable »'
  - index.md: PHP Manual
  - class.phptoken.md: PhpToken
title: 'PhpToken::is'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PhpToken::is

(PHP 8)

PhpToken::is — Перевіряє, чи відповідає токен зазначеному типу

### Опис

```methodsynopsis
public PhpToken::is(int|string|array $kind): bool
```

Перевіряє, чи відповідає токен зазначеному типу `kind`

### Список параметрів

`kind`

Значення порівняння з ідентифікатором токена, чи його текстовим поданням, чи масив таких значень.

### Значення, що повертаються

Логічне значення, **`true`** або **`false`**

### Приклади

**Приклад #1 Приклад використання** PhpToken::is()\*\*\*\*

```php
<?php
$token = new PhpToken(T_ECHO, 'echo');
var_dump($token->is(T_ECHO));        // -> bool(true)
var_dump($token->is('echo'));        // -> bool(true)
var_dump($token->is(T_FOREACH));     // -> bool(false)
var_dump($token->is('foreach'));     // -> bool(false)
```

**Приклад #2 Використання з масивом**

```php
<?php
function isClassType(PhpToken $token): bool {
    return $token->is([T_CLASS, T_INTERFACE, T_TRAIT]);
}

$interface = new PhpToken(T_INTERFACE, 'interface');
var_dump(isClassType($interface));   // -> bool(true)

$function = new PhpToken(T_FUNCTION, 'function');
var_dump(isClassType($function));    // -> bool(false)
```

### Дивіться також

-   [token\_name()](function.token-name.md) \- Отримати символьне ім'я для переданої PHP-лексеми
