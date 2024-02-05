---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-sub.md: « sodium\_crypto\_core\_ristretto255\_scalar\_sub
  - function.sodium-crypto-generichash-final.md: sodium\_crypto\_generichash\_final »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_sub
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_sub

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_sub — Віднімає елемент

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_sub(string $p, string $q): string
```

Віднімає елемент `q`из`p`. Доступно, починаючи з libsodium 1.0.18.

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

**Пример #1 Пример использования**sodium\_crypto\_core\_ristretto255\_sub()\*\*\*\*

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
-   [sodium\_crypto\_core\_ristretto255\_add()](function.sodium-crypto-core-ristretto255-add.md) \- Додає елемент
