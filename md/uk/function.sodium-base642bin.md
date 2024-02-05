---
navigation:
  - function.sodium-add.md: « sodium\_add
  - function.sodium-bin2base64.md: sodium\_bin2base64 »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_base642bin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_base642bin

(PHP 7 >= 7.2.0, PHP 8)

sodium\_base642bin — Перетворює рядок у кодуванні base64 на необроблений двійковий файл

### Опис

```methodsynopsis
sodium_base642bin(string $string, int $id, string $ignore = ""): string
```

Перетворює рядок у кодуванні base64 на необроблений двійковий файл. На відміну від функції [base64\_decode()](function.base64-decode.md), функция**sodium\_base642bin()** постійна за часом (властивість, яка важлива для будь-якого коду, що стосується криптографічних вхідних даних, таких як прості тексти або ключі) і підтримує декілька наборів символів.

### Список параметрів

`string`

Рядок (string); Закодований рядок.

`id`

-   \*\*`SODIUM_BASE64_VARIANT_ORIGINAL`\*\*для стандартного (`A-Za-z0-9/\+`). Кодування Base64.
-   \*\*`SODIUM_BASE64_VARIANT_ORIGINAL_NO_PADDING`\*\*для стандартного (`A-Za-z0-9/\+`) Кодування Base64 без додаткових символів`=`
-   \*\*`SODIUM_BASE64_VARIANT_URLSAFE`\*\*для URL-безпечного (`A-Za-z0-9\-_`). Кодування Base64.
-   \*\*`SODIUM_BASE64_VARIANT_URLSAFE_NO_PADDING`\*\*for URL-safe (`A-Za-z0-9\-_`). Кодування Base64 без додаткових символів`=`

`ignore`

Символи, які слід ігнорувати під час перетворення (наприклад, символи пропуску).

### Значення, що повертаються

Повертає перетворений рядок.
