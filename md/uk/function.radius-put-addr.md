Приєднує атрибут IP-адреси

-   [« radiusgetvendorattr](function.radius-get-vendor-attr.html)
    
-   [radiusputattr »](function.radius-put-attr.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Приєднує атрибут IP-адреси
    

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
> Перед викликом цієї функції потрібно створити запит за допомогою функції [radiuscreaterequest()](function.radius-create-request.html)

### Список параметрів

`radius_handle`

Ресурс RADIUS

`type`

Тип атрибуту.

`addr`

Адреса IPv4 у вигляді рядка, наприклад, `10.0.0.1`

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