---
navigation:
  - function.sodium-crypto-stream.md: « sodiumcryptostream
  - function.sodium-increment.md: sodiumincrement »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumhex2bin
---
# sodiumhex2bin

(PHP 7> = 7.2.0, PHP 8)

sodiumhex2bin - Декодує рядок у шістнадцятковому поданні в бінарне

### Опис

```methodsynopsis
sodium_hex2bin(string $string, string $ignore = ""): string
```

Декодує рядок, закодований у шістнадцяткове подання до бінарного.

Як і [sodiumbin2hex()](function.sodium-bin2hex.md), функція **sodiumhex2bin()** стійка до атак по стороннім каналам (side-channel attacks), на відміну функції [hex2bin()](function.hex2bin.md)

### Список параметрів

`string`

Шістнадцяткове представлення даних.

`ignore`

Необов'язковий рядковий аргумент з символами, що ігноруються.

### Значення, що повертаються

Повертає двійкове подання переданих у аргументі `string` даних.
