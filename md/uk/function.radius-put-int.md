---
navigation:
  - function.radius-put-attr.html: « radiusputattr
  - function.radius-put-string.html: radiusputstring »
  - index.html: PHP Manual
  - ref.radius.html: Функции Radius
title: radiusputint
---
# radiusputint

(PECL radius >= 1.1.0)

radiusputint — Приєднує цілісний атрибут

### Опис

```methodsynopsis
radius_put_int(    resource $radius_handle,    int $type,    int $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує цілий атрибут до поточного запиту RADIUS.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.html)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`value`

Значення атрибуту.

`options`

Бітова маска опцій атрибуту. Як значення можна використовувати [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.html#constant.radius-option-tagged) і [**`RADIUS_OPTION_SALT`**](radius.constants.options.html#constant.radius-option-salt)

`tag`

Тег атрибут. Цей параметр ігнорується, якщо не встановлено опцію [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.html#constant.radius-option-tagged)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL radius 1.3.0 | Додані параметри `options` і `tag` |

### Приклади

**Приклад #1 Приклад використання **radiusputint()****

```php
<?php
if (!radius_put_int($res, RAD_FRAMED_PROTOCOL, RAD_PPP)) {
   echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
   exit;
}
?>
```

### Дивіться також

-   [radiusputstring()](function.radius-put-string.html) - Приєднує рядковий атрибут
-   [radiusputvendorint()](function.radius-put-vendor-int.html) - Приєднує цілий атрибут, що залежить від постачальника
-   [radiusputvendorstring()](function.radius-put-vendor-string.html) - Приєднує рядковий атрибут, що залежить від постачальника
