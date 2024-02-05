---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-reduce.md: « sodium\_crypto\_core\_ristretto255\_scalar\_reduce
  - function.sodium-crypto-core-ristretto255-sub.md: sodium\_crypto\_core\_ristretto255\_sub »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_sub
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_sub

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_sub — Віднімає скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_sub(string $x, string $y): string
```

Віднімає скалярне значення `y`из`x`. Доступно, починаючи з libsodium 1.0.18.

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

**Пример #1 Пример использования**sodium\_crypto\_core\_ristretto255\_scalar\_sub()\*\*\*\*

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
-   [sodium\_crypto\_core\_ristretto255\_scalar\_add()](function.sodium-crypto-core-ristretto255-scalar-add.md) \- Додає скалярне значення
