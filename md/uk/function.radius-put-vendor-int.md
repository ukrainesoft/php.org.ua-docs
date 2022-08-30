Приєднує цілий атрибут, що залежить від постачальника

-   [« radiusputvendorattr](function.radius-put-vendor-attr.html)
    
-   [radiusputvendorstring »](function.radius-put-vendor-string.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Radius](ref.radius.md)
    
-   Приєднує цілий атрибут, що залежить від постачальника
    

# radiusputvendorint

(PECL radius >= 1.1.0)

radiusputvendorint — Приєднує цілий атрибут, що залежить від постачальника.

### Опис

```methodsynopsis
radius_put_vendor_int(    resource $radius_handle,    int $vendor,    int $type,    int $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує до поточного запиту RADIUS цілий атрибут, що залежить від постачальника.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.html)

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

Бітова маска опцій атрибуту. Як значення можна використовувати [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.html#constant.radius-option-tagged) і [**`RADIUS_OPTION_SALT`**](radius.constants.options.html#constant.radius-option-salt)

`tag`

Тег атрибут. Цей параметр ігнорується, якщо не встановлено опцію [**`RADIUS_OPTION_TAGGED`**](radius.constants.options.html#constant.radius-option-tagged)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия            | Описание                           |
|-------------------|------------------------------------|
| PECL radius 1.3.0 | Додані параметри `options` і `tag` |

### Дивіться також

-   [radiusputvendorstring()](function.radius-put-vendor-string.html) - Приєднує рядковий атрибут, що залежить від постачальника