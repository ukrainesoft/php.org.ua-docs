---
navigation:
  - function.radius-put-vendor-string.md: « radiusputvendorstring
  - function.radius-salt-encrypt-attr.md: radiussaltencryptattr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusrequestauthenticator
---
# radiusrequestauthenticator

(PECL radius >= 1.1.0)

radiusrequestauthenticator — Повертає автентифікатор запиту

### Опис

```methodsynopsis
radius_request_authenticator(resource $radius_handle): string
```

Аутентифікатор запиту необхідний для розпізнавання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає автентифікатор запиту у вигляді рядка або **`false`** у разі виникнення помилки.

### Дивіться також

-   [radiusdemangle()](function.radius-demangle.md) - Розшифровує дані
