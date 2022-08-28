Приєднує рядковий атрибут, що залежить від постачальника

-   [« radius\_put\_vendor\_int](function.radius-put-vendor-int.html)
    
-   [radius\_request\_authenticator »](function.radius-request-authenticator.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Приєднує рядковий атрибут, що залежить від постачальника
    

# radiusputvendorstring

(PECL radius >= 1.1.0)

radiusputvendorstring — Приєднує рядковий атрибут, що залежить від постачальника

### Опис

```methodsynopsis
radius_put_vendor_string(    resource $radius_handle,    int $vendor,    int $type,    string $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує до поточного запиту рядковий атрибут RADIUS, що залежить від постачальника. В загальному, [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.html) - корисніша функція для приєднання рядкових атрибутів, оскільки вона бінарно безпечна.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radius\_create\_request()](function.radius-create-request.html)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`vendor`

ID виробника (Vendor).

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

### Дивіться також

-   [radius\_put\_vendor\_int()](function.radius-put-vendor-int.html) - Приєднує цілий атрибут, що залежить від постачальника