---
navigation:
  - function.radius-get-vendor-attr.md: « radiusgetvendorattr
  - function.radius-put-attr.md: radiusputattr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusputaddr
---
# radiusputaddr

(PECL radius >= 1.1.0)

radiusputaddr — Приєднує атрибут IP-адреси

### Опис

```methodsynopsis
radius_put_addr(    resource $radius_handle,    int $type,    string $addr,    int $options = 0,    int $tag = ?): bool
```

Приєднує атрибут IP-адреси до запиту RADIUS.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.md)

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

Тег атрибут. Цей параметр ігнорується, якщо не встановлено опцію [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL radius 1.3.0 | Додані параметри `options` і `tag` |
