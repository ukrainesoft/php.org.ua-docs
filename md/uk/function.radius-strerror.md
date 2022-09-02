---
navigation:
  - function.radius-server-secret.md: « radiusserversecret
  - refs.utilspec.cmdline.md: Модулі для роботи з командним рядком »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusstrerror
---
# radiusstrerror

(PECL radius >= 1.1.0)

radiusstrerror — Повертає повідомлення про помилку

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
