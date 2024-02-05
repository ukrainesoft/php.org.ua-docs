---
navigation:
  - function.sodium-crypto-core-ristretto255-random.md: « sodium\_crypto\_core\_ristretto255\_random
  - function.sodium-crypto-core-ristretto255-scalar-complement.md: sodium\_crypto\_core\_ristretto255\_scalar\_complement »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_add

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_add — Додає скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_add(string $x, string $y): string
```

Додає елемент `y`к`x`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_core\_ristretto255\_scalar\_add()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_core_ristretto255_scalar_random();

$value = sodium_crypto_core_ristretto255_scalar_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_scalar_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md) \- Генерує випадковий ключ
-   [sodium\_crypto\_core\_ristretto255\_scalar\_sub()](function.sodium-crypto-core-ristretto255-scalar-sub.md) \- Віднімає скалярне значення
