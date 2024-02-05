---
navigation:
  - function.ldap-close.md: « ldap\_close
  - function.ldap-connect-wallet.md: ldap\_connect\_wallet »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_compare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_compare

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

ldap\_compare — Порівняти атрибут, знайдений у записі певної DN

### Опис

```methodsynopsis
ldap_compare(    LDAP\Connection $ldap,    string $dn,    string $attribute,    string $value,    ?array $controls = null): bool|int
```

Порівнює значення (`value`) атрибуту (`attribute`) зі значенням того ж атрибуту запису LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Відмінне ім'я об'єкта LDAP.

`attribute`

Ім'я атрибуту.

`value`

Порівнюване значення.

`controls`

Массив[керуючих констант LDAP](ldap.controls.md)для отправки в запросе.

### Значення, що повертаються

Повертає **`true`** якщо `value` збігаються в іншому випадку **`false`**. Повертає -1 у разі помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Приклади

Наступний приклад демонструє, як перевірити, чи збігається цей пароль з тим, який визначено у зазначеному записі DN.

**Приклад #1 Повний приклад перевірки пароля**

```php
<?php

$ds=ldap_connect("localhost");  // Предположим, что LDAP сервер находится по этому адресу

if ($ds) {

    // bind
    if (ldap_bind($ds)) {

        // подготовка данных
        $dn = "cn=Matti Meikku, ou=My Unit, o=My Company, c=FI";
        $value = "secretpassword";
        $attr = "password";

        // сравнение данных
        $r=ldap_compare($ds, $dn, $attr, $value);

        if ($r === -1) {
            echo "Ошибка: " . ldap_error($ds);
        } elseif ($r === true) {
            echo "Пароль верный.";
        } elseif ($r === false) {
            echo "Неправильное предположение! Пароль не верен.";
        }

    } else {
        echo "Невозможно привязаться к серверу LDAP.";
    }

    ldap_close($ds);

} else {
    echo "Невозможно соединиться с сервером LDAP.";
}
?>
```

### Примітки

**Увага**

**ldap\_compare()** не може бути використана для порівняння бінарних (BINARY) значень!
