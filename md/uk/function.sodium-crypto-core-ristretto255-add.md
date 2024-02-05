---
navigation:
  - function.sodium-crypto-box.md: « sodium\_crypto\_box
  - function.sodium-crypto-core-ristretto255-from-hash.md: sodium\_crypto\_core\_ristretto255\_from\_hash »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_add

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_add — Додає елемент

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_add(string $p, string $q): string
```

Додає елемент `q`к`p`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`p`

Елемент.

`q`

Елемент.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_core\_ristretto255\_add()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_random();
$bar = sodium_crypto_core_ristretto255_random();

$value = sodium_crypto_core_ristretto255_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_random()](function.sodium-crypto-core-ristretto255-random.md) \- Генерує випадковий ключ
-   [sodium\_crypto\_core\_ristretto255\_sub()](function.sodium-crypto-core-ristretto255-sub.md) \- Віднімає елемент
