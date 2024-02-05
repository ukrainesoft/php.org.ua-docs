---
navigation:
  - function.radius-put-vendor-attr.md: « radius\_put\_vendor\_attr
  - function.radius-put-vendor-string.md: radius\_put\_vendor\_string »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_put\_vendor\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_put\_vendor\_int

(PECL radius >= 1.1.0)

radius\_put\_vendor\_int — Приєднує цілий атрибут від постачальника.

### Опис

```methodsynopsis
radius_put_vendor_int(    resource $radius_handle,    int $vendor,    int $type,    int $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує до поточного запиту RADIUS цілий атрибут, що залежить від постачальника.

> **Зауваження** :
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radius\_create\_request()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`vendor`

ID виробника (Vendor).

`type`

Тип атрибуту.

`value`

Значення атрибуту.

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

### Дивіться також

-   [radius\_put\_vendor\_string()](function.radius-put-vendor-string.md) \- Приєднує рядковий атрибут, що залежить від постачальника
