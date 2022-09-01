---
navigation:
  - function.radius-send-request.html: « radiussendrequest
  - function.radius-strerror.html: radiusstrerror »
  - index.html: PHP Manual
  - ref.radius.html: Функции Radius
title: radiusserversecret
---
# radiusserversecret

(PECL radius >= 1.1.0)

radiusserversecret — Повертає загальний секрет

### Опис

```methodsynopsis
radius_server_secret(resource $radius_handle): string
```

Загальний секрет необхідний як сіль для розбирання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає загальний секрет сервера у вигляді рядка або **`false`** у разі виникнення помилки.
