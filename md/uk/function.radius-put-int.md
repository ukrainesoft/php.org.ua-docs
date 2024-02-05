---
navigation:
  - function.radius-put-attr.md: « radius\_put\_attr
  - function.radius-put-string.md: radius\_put\_string »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_put\_int
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_put\_int

(PECL radius >= 1.1.0)

radius\_put\_int — Приєднує цілісний атрибут

### Опис

```methodsynopsis
radius_put_int(    resource $radius_handle,    int $type,    int $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує цілий атрибут до поточного запиту RADIUS.

> **Зауваження** :
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radius\_create\_request()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

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

### Приклади

**Пример #1 Пример использования**radius\_put\_int()\*\*\*\*

```php
<?php
if (!radius_put_int($res, RAD_FRAMED_PROTOCOL, RAD_PPP)) {
   echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
   exit;
}
?>
```

### Дивіться також

-   [radius\_put\_string()](function.radius-put-string.md) \- Приєднує рядковий атрибут
-   [radius\_put\_vendor\_int()](function.radius-put-vendor-int.md) \- Приєднує цілий атрибут, що залежить від постачальника
-   [radius\_put\_vendor\_string()](function.radius-put-vendor-string.md) \- Приєднує рядковий атрибут, що залежить від постачальника
