---
navigation:
  - function.radius-put-int.html: « radiusputint
  - function.radius-put-vendor-addr.html: radiusputvendoraddr »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiusputstring
---
# radiusputstring

(PECL radius >= 1.1.0)

radiusputstring — Приєднує рядковий атрибут

### Опис

```methodsynopsis
radius_put_string(    resource $radius_handle,    int $type,    string $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує строковий атрибут до поточного запиту RADIUS. В загальному, [radiusputattr()](function.radius-put-attr.md) - корисніша функція для приєднання рядкових атрибутів, оскільки вона бінарно безпечна.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`value`

Значення атрибуту. Базова бібліотека очікує, що це значення матиме нульовий символ наприкінці, тому цей параметр є небезпечним для двійкового коду.

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

**Приклад #1 Приклад використання **radiusputstring()****

```php
<?php
if (!radius_put_string($res, RADIUS_USER_NAME, 'billy')) {
    echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radiusputint()](function.radius-put-int.md) - Приєднує цілісний атрибут
-   [radiusputvendorint()](function.radius-put-vendor-int.md) - Приєднує цілий атрибут, що залежить від постачальника
-   [radiusputvendorstring()](function.radius-put-vendor-string.md) - Приєднує рядковий атрибут, що залежить від постачальника
