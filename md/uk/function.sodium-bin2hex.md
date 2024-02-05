---
navigation:
  - function.sodium-bin2base64.md: « sodium\_bin2base64
  - function.sodium-compare.md: sodium\_compare »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_bin2hex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_bin2hex

(PHP 7 >= 7.2.0, PHP 8)

sodium\_bin2hex — Кодувати в шістнадцяткову виставу

### Опис

```methodsynopsis
sodium_bin2hex(string $string): string
```

Перетворює необроблений двійковий рядок у рядок у шістнадцятковому кодуванні. На відміну від стандартної функції шістнадцяткового кодування, **sodium\_bin2hex()** є постійною за часом (властивість, яка є важливою для будь-якого коду, який стосується криптографічних даних, таких як тексти або ключі).

### Список параметрів

`string`

Необроблений двійковий рядок.

### Значення, що повертаються

Рядок у шістнадцятковому коді.
