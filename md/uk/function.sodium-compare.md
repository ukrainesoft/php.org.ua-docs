---
navigation:
  - function.sodium-bin2hex.md: « sodiumbin2hex
  - function.sodium-crypto-aead-aes256gcm-decrypt.md: sodiumcryptoaeadaes256gcmdecrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcompare
---
# sodiumcompare

(PHP 7> = 7.2.0, PHP 8)

sodiumcompare — Порівняти великі числа

### Опис

```methodsynopsis
sodium_compare(string $string1, string $string2): int
```

Порівнює два рядки, ніби вони були цілими числами довільної довжини без знака з прямим порядком байтів, без витоку з побічного каналу.

### Список параметрів

`string1`

Лівий операнд

`string2`

Правий операнд

### Значення, що повертаються

Повертає `-1`, якщо `string1` менше `string2`

Повертає `1`, якщо `string1` більше `string2`

Повертає `0`якщо рядки рівні.
