---
navigation:
  - function.sodium-crypto-core-ristretto255-is-valid-point.html: « sodiumcryptocoreristretto255ісvalidpoint
  - function.sodium-crypto-core-ristretto255-scalar-add.html: sodiumcryptocoreristretto255scalaradd »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255random
---
# sodiumcryptocoreristretto255random

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255random - Генерує випадковий ключ

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_random(): string
```

Генерує випадковий ключ. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255random()****

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

-   [sodiumcryptocoreristretto255add()](function.sodium-crypto-core-ristretto255-add.md) - Додає елемент
-   [sodiumcryptocoreristretto255sub()](function.sodium-crypto-core-ristretto255-sub.md) - Віднімає елемент
