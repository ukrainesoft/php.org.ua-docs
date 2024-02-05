---
navigation:
  - function.sodium-crypto-core-ristretto255-add.md: « sodium\_crypto\_core\_ristretto255\_add
  - function.sodium-crypto-core-ristretto255-is-valid-point.md: sodium\_crypto\_core\_ristretto255\_is\_valid\_point »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_from\_hash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_from\_hash

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_from\_hash — Порівняє вектор

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_from_hash(string $s): string
```

Зіставляє вектор 64-байтовий вектор `s` з елементом групи. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`s`

64-байт вектор.

### Значення, що повертаються

Повертає 32-байтовий випадковий рядок (string).

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_core\_ristretto255\_from\_hash()\*\*\*\*

```php
<?php

$hashes = sodium_hex2bin(
    '5d1be09e3d0c82fc538112490e35701979d99e06ca3e2b5b54bffe8b4dc772c1' .
    '4d98b696a1bbfb5ca32c436cc61c16563790306c79eaca7705668b47dffe5bb6'
);
var_dump(sodium_bin2hex(sodium_crypto_core_ristretto255_from_hash($hashes)));
?>
```

Результат виконання наведеного прикладу:

```
string(64) "3066f82a1a747d45120d1740f14358531a8f04bbffe6a819f86dfe50f44a0a46"
```

### Дивіться також

-   [sodium\_hex2bin()](function.sodium-hex2bin.md) \- Декодує рядок у шістнадцятковому поданні до бінарного
-   [sodium\_bin2hex()](function.sodium-bin2hex.md) \- Кодувати у шістнадцяткову виставу
-   **sodium\_crypto\_core\_ristretto255\_from\_hash()**
