---
navigation:
  - function.radius-put-vendor-addr.md: « radiusputvendoraddr
  - function.radius-put-vendor-int.md: radiusputvendorint »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusputvendorattr
---
# radiusputvendorattr

(PECL radius >= 1.1.0)

radiusputvendorattr — Приєднує бінарний атрибут, що залежить від постачальника

### Опис

```methodsynopsis
radius_put_vendor_attr(    resource $radius_handle,    int $vendor,    int $type,    string $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує до поточного запиту RADIUS бінарний атрибут, що залежить від постачальника.

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

`value`

Значення атрибуту, яке розглядатиметься як необроблений двійковий рядок.

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

### Приклади

**Приклад #1 Приклад використання **radiusputvendorattr()****

```php
<?php
if (!radius_put_vendor_attr($res, RADIUS_VENDOR_MICROSOFT, RAD_MICROSOFT_MS_CHAP_CHALLENGE, $challenge)) {
    echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radiusgetvendorattr()](function.radius-get-vendor-attr.md) - Витягує атрибут, що залежить від постачальника
