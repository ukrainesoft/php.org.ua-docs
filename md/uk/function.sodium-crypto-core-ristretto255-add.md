---
navigation:
  - function.sodium-crypto-box.md: « sodiumcryptobox
  - function.sodium-crypto-core-ristretto255-from-hash.md: sodiumcryptocoreristretto255fromhash »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255add
---
# sodiumcryptocoreristretto255add

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255add — Додає елемент

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_add(string $p, string $q): string
```

Додає елемент `q` до `p`. Доступно, починаючи з libsodium 1.0.18.

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

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255add()****

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
-   [sodiumcryptocoreristretto255sub()](function.sodium-crypto-core-ristretto255-sub.md) - Віднімає елемент
