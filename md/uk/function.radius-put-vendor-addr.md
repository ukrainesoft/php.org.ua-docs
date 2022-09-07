---
navigation:
  - function.radius-put-string.md: « radiusputstring
  - function.radius-put-vendor-attr.md: radiusputvendorattr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusputvendoraddr
---
# radiusputvendoraddr

(PECL radius >= 1.1.0)

radiusputvendoraddr — Приєднує атрибут IP-адреси до конкретного постачальника.

### Опис

```methodsynopsis
radius_put_vendor_addr(    resource $radius_handle,    int $vendor,    int $type,    string $addr): bool
```

Приєднує атрибут постачальника IP-адреси до поточного запиту RADIUS.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`vendor`

ID виробника (Vendor).

`type`

Тип атрибуту.

`addr`

Адреса IPv4 у вигляді рядка, наприклад, `10.0.0.1`

`options`

Бітова маска опцій атрибуту. Як значення можна використовувати [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged) і [**`RADIUS_OPTION_SALT`**](radius.constants.options.md#constant.radius-option-salt)

`tag`

Тег атрибут. Цей параметр ігнорується, якщо не встановлено опцію [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL radius 1.3.0 | Додані параметри `options` і `tag` |
