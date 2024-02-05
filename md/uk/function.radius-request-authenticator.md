---
navigation:
  - function.radius-put-vendor-string.md: « radius\_put\_vendor\_string
  - function.radius-salt-encrypt-attr.md: radius\_salt\_encrypt\_attr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_request\_authenticator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_request\_authenticator

(PECL radius >= 1.1.0)

radius\_request\_authenticator — Повертає автентифікатор запиту

### Опис

```methodsynopsis
radius_request_authenticator(resource $radius_handle): string
```

Аутентифікатор запиту необхідний для розпізнавання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає автентифікатор запиту у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [radius\_demangle()](function.radius-demangle.md) \- Розшифровує дані
