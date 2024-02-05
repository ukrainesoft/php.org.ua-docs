---
navigation:
  - function.sodium-crypto-stream.md: « sodium\_crypto\_stream
  - function.sodium-increment.md: sodium\_increment »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_hex2bin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_hex2bin

(PHP 7 >= 7.2.0, PHP 8)

sodium\_hex2bin - Декодує рядок у шістнадцятковому поданні в бінарне

### Опис

```methodsynopsis
sodium_hex2bin(string $string, string $ignore = ""): string
```

Декодує рядок, закодований у шістнадцяткове подання до бінарного.

Як і [sodium\_bin2hex()](function.sodium-bin2hex.md), функция**sodium\_hex2bin()** стійка до атак по стороннім каналам (side-channel attacks), на відміну функції [hex2bin()](function.hex2bin.md)

### Список параметрів

`string`

Шістнадцяткове представлення даних.

`ignore`

Необов'язковий рядковий аргумент з символами, що ігноруються.

### Значення, що повертаються

Повертає двійкове подання переданих у аргументі `string` даних.
