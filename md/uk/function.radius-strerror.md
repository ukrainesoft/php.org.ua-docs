---
navigation:
  - function.radius-server-secret.md: « radius\_server\_secret
  - refs.utilspec.cmdline.md: Модулі для роботи з командним рядком »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_strerror

(PECL radius >= 1.1.0)

radius\_strerror — Повертає повідомлення про помилку

### Опис

```methodsynopsis
radius_strerror(resource $radius_handle): string
```

У разі помилки функцій radius, вони записують повідомлення про помилку. Це повідомлення можна отримати за допомогою цієї функції.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Повертає повідомлення про помилки у вигляді рядка з функцій radius, що завершилися помилкою.
