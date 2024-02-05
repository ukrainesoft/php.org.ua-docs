---
navigation:
  - function.radius-cvt-string.md: « radius\_cvt\_string
  - function.radius-demangle.md: radius\_demangle »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_demangle\_mppe\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_demangle\_mppe\_key

(PECL radius >= 1.2.0)

radius\_demangle\_mppe\_key — Отримує mppe-ключі зі спотворених даних

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

Повертає деформований рядок або \*\*`false`\*\*в случае возникновения ошибки.
