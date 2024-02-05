---
navigation:
  - function.sodium-bin2hex.md: « sodium\_bin2hex
  - function.sodium-crypto-aead-aes256gcm-decrypt.md: sodium\_crypto\_aead\_aes256gcm\_decrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_compare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_compare

(PHP 7 >= 7.2.0, PHP 8)

sodium\_compare — Порівняти великі числа

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

Повертає `-1`, якщо `string1`меньше`string2`

Повертає , якщо `string1`больше`string2`

Повертає якщо рядки рівні.
