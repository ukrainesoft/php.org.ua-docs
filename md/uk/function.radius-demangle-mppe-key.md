---
navigation:
  - function.radius-cvt-string.md: « radiuscvtstring
  - function.radius-demangle.md: radiusdemangle »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusdemanglemppekey
---
# radiusdemanglemppekey

(PECL radius >= 1.2.0)

radiusdemanglemppekey — Отримує mppe-ключі зі спотворених даних

### Опис

```methodsynopsis
radius_demangle_mppe_key(resource $radius_handle, string $mangled): string
```

При використанні MPPE з MS-CHAPv2 ключі відправляються та одержувані ключі спотворюються (дивіться [» RFC 2548](http://www.faqs.org/rfcs/rfc2548)), однак ця функція не є корисною, оскільки я не думаю, що є або буде реалізація PPTP-MPPE в PHP.

### Список параметрів

`radius_handle`

Ресурс RADIUS

`mangled`

Спотворені дані, які необхідно деформувати

### Значення, що повертаються

Повертає деформований рядок або **`false`** у разі виникнення помилки.
