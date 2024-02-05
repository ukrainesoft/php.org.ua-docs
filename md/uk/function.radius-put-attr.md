---
navigation:
  - function.radius-put-addr.md: « radius\_put\_addr
  - function.radius-put-int.md: radius\_put\_int »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_put\_attr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_put\_attr

(PECL radius >= 1.1.0)

radius\_put\_attr - Приєднує бінарний атрибут

### Опис

```methodsynopsis
radius_put_attr(    resource $radius_handle,    int $type,    string $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує бінарний атрибут до запиту RADIUS.

> **Зауваження** :
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radius\_create\_request()](function.radius-create-request.md)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`value`

Значення атрибуту, яке розглядатиметься як необроблений двійковий рядок.

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

**Пример #1 Пример использования**radius\_put\_attr()\*\*\*\*

```php
<?php
mt_srand(time());
$chall = mt_rand();
$chapval = md5(pack('Ca*',1 , 'sepp' . $chall));
$pass = pack('CH*', 1, $chapval);
if (!radius_put_attr($res, RADIUS_CHAP_PASSWORD, $pass)) {
    echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radius\_get\_attr()](function.radius-get-attr.md) \- Витягує атрибут
-   [radius\_get\_vendor\_attr()](function.radius-get-vendor-attr.md) \- Витягує атрибут, що залежить від постачальника
-   [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.md) \- Приєднує бінарний атрибут, що залежить від постачальника
