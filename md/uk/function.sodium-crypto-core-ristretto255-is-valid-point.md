---
navigation:
  - function.sodium-crypto-core-ristretto255-from-hash.md: « sodium\_crypto\_core\_ristretto255\_from\_hash
  - function.sodium-crypto-core-ristretto255-random.md: sodium\_crypto\_core\_ristretto255\_random »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_is\_valid\_point
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_is\_valid\_point

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_is\_valid\_point — Визначає, чи лежить точка на кривій ristretto255

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_is_valid_point(string $s): bool
```

Визначає, чи лежить точка на кривій ristretto255 у канонічній формі на головній підгрупі і що точка не має малого порядку. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`s`

Крапка еліптичної кривої.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо точка `s` знаходиться на кривій ristretto255, інакше повертає\*\*`false`\*\*.

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_core\_ristretto255\_is\_valid\_point()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_scalarmult_ristretto255_base($foo);

var_dump(sodium_crypto_core_ristretto255_is_valid_point($bar));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md) \- Генерує випадковий ключ
-   [sodium\_crypto\_scalarmult\_ristretto255\_base()](function.sodium-crypto-scalarmult-ristretto255-base.md) \- Обчислює відкритий ключ із закритого ключа
