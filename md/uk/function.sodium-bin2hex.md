---
navigation:
  - function.sodium-bin2base64.html: « sodiumbin2base64
  - function.sodium-compare.html: sodiumcompare »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumbin2hex
---
# sodiumbin2hex

(PHP 7> = 7.2.0, PHP 8)

sodiumbin2hex — Кодувати в шістнадцяткову виставу

### Опис

```methodsynopsis
sodium_bin2hex(string $string): string
```

Перетворює необроблений двійковий рядок у рядок у шістнадцятковому кодуванні. На відміну від стандартної функції шістнадцяткового кодування, **sodiumbin2hex()** є постійною за часом (властивість, яка важлива для будь-якого коду, який стосується криптографічних даних, таких як тексти чи ключі).

### Список параметрів

`string`

Необроблений двійковий рядок.

### Значення, що повертаються

Рядок у шістнадцятковому коді.
