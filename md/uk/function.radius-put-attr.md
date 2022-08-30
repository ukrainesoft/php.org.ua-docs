Приєднує бінарний атрибут

-   [« radiusputaddr](function.radius-put-addr.html)
    
-   [radiusputint »](function.radius-put-int.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Приєднує бінарний атрибут
    

# radiusputattr

(PECL radius >= 1.1.0)

radiusputattr - Приєднує бінарний атрибут

### Опис

```methodsynopsis
radius_put_attr(    resource $radius_handle,    int $type,    string $value,    int $options = 0,    int $tag = ?): bool
```

Приєднує бінарний атрибут до запиту RADIUS.

> **Зауваження**
> 
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.html)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`value`

Значення атрибуту, яке розглядатиметься як необроблений двійковий рядок.

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

### Приклади

**Приклад #1 Приклад використання **radiusputattr()****

```php
<?php
mt_srand(time());
$chall = mt_rand();
$chapval = md5(pack('Ca*',1 , 'sepp' . $chall));
$pass = pack('CH*', 1, $chapval);
if (!radius_put_attr($res, RADIUS_CHAP_PASSWORD, $pass)) {
    echo 'Ошибка Radius:' . radius_strerror($res). "\n<br />";
    exit;
}
?>
```

### Дивіться також

-   [radiusgetattr()](function.radius-get-attr.html) - Витягує атрибут
-   [radiusgetvendorattr()](function.radius-get-vendor-attr.html) - Витягує атрибут, що залежить від постачальника
-   [radiusputvendorattr()](function.radius-put-vendor-attr.html) - Приєднує бінарний атрибут, що залежить від постачальника