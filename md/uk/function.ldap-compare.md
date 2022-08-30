Порівняти значення атрибута, знайденого у записі певної DN

-   [« ldapclose](function.ldap-close.html)
    
-   [ldapconnect »](function.ldap-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Порівняти значення атрибута, знайденого у записі певної DN
    

# ldapcompare

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

ldapcompare — Порівняти значення атрибута, знайденого в записі певної DN

### Опис

```methodsynopsis
ldap_compare(    LDAP\Connection $ldap,    string $dn,    string $attribute,    string $value,    ?array $controls = null): bool|int
```

Порівнює значення (`value`) атрибуту (`attribute`) зі значенням того ж атрибуту запису LDAP-директорії.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

Відмінне ім'я об'єкта LDAP.

`attribute`

Ім'я атрибуту.

`value`

Порівнюване значення.

`controls`

Масив [управляющих констант LDAP](ldap.controls.html) для відправки у запиті.

### Значення, що повертаються

Повертає **`true`** якщо `value` збігаються в іншому випадку **`false`**. Повертає -1 у разі помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | `controls` тепер припускає значення null; раніше значення за умовчанням було `[]`                                                                      |
|        | Додано підтримку параметра `controls`                                                                                                                  |

### Приклади

Наступний приклад демонструє, як перевірити, чи збігається цей пароль з тим, який визначено у зазначеному записі DN.

**Приклад #1 Повний приклад перевірки пароля**

```php
<?php

$ds=ldap_connect("localhost");  // Предположим, что LDAP сервер находится по этому адресу

if ($ds) {

    // bind
    if (ldap_bind($ds)) {

        // подготовка данных
        $dn = "cn=Matti Meikku, ou=My Unit, o=My Company, c=FI";
        $value = "secretpassword";
        $attr = "password";

        // сравнение данных
        $r=ldap_compare($ds, $dn, $attr, $value);

        if ($r === -1) {
            echo "Ошибка: " . ldap_error($ds);
        } elseif ($r === true) {
            echo "Пароль верный.";
        } elseif ($r === false) {
            echo "Неправильное предположение! Пароль не верен.";
        }

    } else {
        echo "Невозможно привязаться к серверу LDAP.";
    }

    ldap_close($ds);

} else {
    echo "Невозможно соединиться с сервером LDAP.";
}
?>
```

### Примітки

**Увага**

**ldapcompare()** не може бути використана для порівняння бінарних (BINARY) значень!