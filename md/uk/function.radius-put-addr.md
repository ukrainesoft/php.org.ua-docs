- [«radius_get_vendor_attr](function.radius-get-vendor-attr.md)
- [radius_put_attr »](function.radius-put-attr.md)

- [PHP Manual](index.md)
- [Функції Radius](ref.radius.md)
- Приєднує атрибут IP-адреси

#radius_put_addr

(PECL radius \>= 1.1.0)

radius_put_addr — Приєднує атрибут IP-адреси

### Опис

**radius_put_addr**(
resource `$radius_handle`,
int `$type`,
string `$addr`,
int `$options` = 0,
int `$tag` = ?
): bool

Приєднує атрибут IP-адреси до запиту RADIUS.

> **Примітка**:
>
> Перед викликом цієї функції необхідно створити запит за допомогою
> функції
> [radius_create_request()](function.radius-create-request.md).

### Список параметрів

`radius_handle`
Ресурс RADIUS

`type`
Тип атрибуту.

`addr`
Адреса IPv4 у вигляді рядка, наприклад, `10.0.0.1`.

`options`
Бітова маска опцій атрибуту. Як значення можна використовувати
[**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged)
і
[**`RADIUS_OPTION_SALT`**](radius.constants.options.md#constant.radius-option-salt).

`tag`
Тег атрибут. Цей параметр ігнорується, якщо не встановлено опцію
[**`RADIUS_OPTION_TAGGED`**](radius.constants.options.md#constant.radius-option-tagged).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія                                             | Опис |
|----------------------------------------------------|------|
| PECL radius 1.3.0 Додані параметри options та tag. |      |
