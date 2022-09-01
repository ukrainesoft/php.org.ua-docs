---
navigation:
  - function.sodium-base642bin.html: « sodiumbase642bin
  - function.sodium-bin2hex.html: sodiumbin2hex »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumbin2base64
---
# sodiumbin2base64

(PHP 7> = 7.2.0, PHP 8)

sodiumbin2base64 — Кодує необроблений двійковий рядок за допомогою base64

### Опис

```methodsynopsis
sodium_bin2base64(string $string, int $id): string
```

Перетворює необроблений двійковий рядок у рядок у кодуванні base64. На відміну від [base64encode()](function.base64-encode.md) **sodiumbin2base64()** є постійною за часом (властивість, яка важлива для будь-якого коду, що стосується криптографічних вхідних даних, таких як прості тексти або ключі), і підтримує кілька наборів символів.

### Список параметрів

`string`

Необроблений двійковий рядок.

`id`

-   **`SODIUM_BASE64_VARIANT_ORIGINAL`** для стандартного (`A-Za-z0-9/\+`) Кодування Base64.
-   **`SODIUM_BASE64_VARIANT_ORIGINAL_NO_PADDING`** for standard (`A-Za-z0-9/\+`) Кодування Base64 без додаткових символів `=`
-   **`SODIUM_BASE64_VARIANT_URLSAFE`** для URL-безпечного (`A-Za-z0-9\-_`) Кодування Base64.
-   **`SODIUM_BASE64_VARIANT_URLSAFE_NO_PADDING`** для URL-безпечного (`A-Za-z0-9\-_`) Кодування Base64 без додаткових символів `=`

### Значення, що повертаються

Рядок у кодуванні Base64.
