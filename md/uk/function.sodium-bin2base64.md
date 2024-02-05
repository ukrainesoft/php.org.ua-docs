---
navigation:
  - function.sodium-base642bin.md: « sodium\_base642bin
  - function.sodium-bin2hex.md: sodium\_bin2hex »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_bin2base64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_bin2base64

(PHP 7 >= 7.2.0, PHP 8)

sodium\_bin2base64 — Кодує необроблений двійковий рядок за допомогою base64

### Опис

```methodsynopsis
sodium_bin2base64(string $string, int $id): string
```

Перетворює необроблений двійковий рядок у рядок у кодуванні base64. На відміну від функції [base64\_encode()](function.base64-encode.md), функция**sodium\_bin2base64()** постійна за часом (властивість, яка важлива для будь-якого коду, що стосується криптографічних вхідних даних, таких як прості тексти або ключі), і підтримує кілька наборів символів.

### Список параметрів

`string`

Необроблений двійковий рядок.

`id`

-   \*\*`SODIUM_BASE64_VARIANT_ORIGINAL`\*\*для стандартного (`A-Za-z0-9/\+`) Кодування Base64.
-   \*\*`SODIUM_BASE64_VARIANT_ORIGINAL_NO_PADDING`\*\*for standard (`A-Za-z0-9/\+`) Кодування Base64 без додаткових символів`=`
-   \*\*`SODIUM_BASE64_VARIANT_URLSAFE`\*\*для URL-безпечного (`A-Za-z0-9\-_`) Кодування Base64.
-   \*\*`SODIUM_BASE64_VARIANT_URLSAFE_NO_PADDING`\*\*для URL-безпечного (`A-Za-z0-9\-_`) Кодування Base64 без додаткових символів`=`

### Значення, що повертаються

Повертає рядок у кодуванні Base64.
