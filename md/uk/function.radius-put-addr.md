---
navigation:
  - function.radius-get-vendor-attr.md: « radius\_get\_vendor\_attr
  - function.radius-put-attr.md: radius\_put\_attr »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_put\_addr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_put\_addr

(PECL radius >= 1.1.0)

radius\_put\_addr — Приєднує атрибут IP-адреси

### Опис

```methodsynopsis
radius_put_addr(    resource $radius_handle,    int $type,    string $addr,    int $options = 0,    int $tag = ?): bool
```

Приєднує атрибут IP-адреси до запиту RADIUS.

> **Зауваження** :
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radius\_create\_request()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`addr`

Адреса IPv4 у вигляді рядка, наприклад, `10.0.0.1`

`options`

Бітова маска опцій атрибуту. Як значення можна використовувати [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged) і [**`RADIUS_OPTION_SALT`**](radius.constants.options.md#constant.radius-option-salt)

`tag`

Тег атрибут. Цей параметр буде проігноровано, якщо не встановлено опцію [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL radius 1.3.0 | Додані параметри `options`и`tag` |
