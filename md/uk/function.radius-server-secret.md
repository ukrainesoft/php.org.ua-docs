---
navigation:
  - function.radius-send-request.md: « radius\_send\_request
  - function.radius-strerror.md: radius\_strerror »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_server\_secret
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_server\_secret

(PECL radius >= 1.1.0)

radius\_server\_secret — Повертає загальний секрет

### Опис

```methodsynopsis
radius_server_secret(resource $radius_handle): string
```

Загальний секрет необхідний як сіль для розбирання спотворених даних, таких як паролі та ключі шифрування.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає загальний секрет сервера у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.
