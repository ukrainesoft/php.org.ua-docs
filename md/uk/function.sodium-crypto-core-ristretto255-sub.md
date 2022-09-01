---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-sub.html: « sodiumcryptocoreristretto255scalarsub
  - function.sodium-crypto-generichash-final.html: sodiumcryptogenerichashfinal »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255sub
---
# sodiumcryptocoreristretto255sub

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255sub — Віднімає елемент

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_sub(string $p, string $q): string
```

Віднімає елемент `q` з `p`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`p`

Елемент.

`q`

Елемент.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255sub()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_random();
$bar = sodium_crypto_core_ristretto255_random();

$value = sodium_crypto_core_ristretto255_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodiumcryptocoreristretto255random()](function.sodium-crypto-core-ristretto255-random.md) - Генерує випадковий ключ
-   [sodiumcryptocoreristretto255add()](function.sodium-crypto-core-ristretto255-add.md) - Додає елемент
