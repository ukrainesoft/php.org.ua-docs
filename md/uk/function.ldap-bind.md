Прив'язати до LDAP директорії

-   [« ldapbindext](function.ldap-bind-ext.html)
    
-   [ldapclose »](function.ldap-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функції LDAP](ref.ldap.html)
    
-   Прив'язати до LDAP директорії
    

# ldapbind

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapbind — Прив'язати до LDAP директорії

### Опис

```methodsynopsis
ldap_bind(LDAP\Connection $ldap, ?string $dn = null, ?string $password = null): bool
```

Зв'язує LDAP-директорію із зазначеним RDN та паролем.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.html), що повертається функцією [ldapconnect()](function.ldap-connect.html)

`dn`

`password`

Якщо `password` не визначено, то буде спроба анонімної прив'язки. Також для анонімної прив'язки можна залишити порожнім `dn`, як визначено в [https://tools.ietf.org/html/rfc2251#section-4.2.2](https://tools.ietf.org/html/rfc2251#section-4.2.2)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання прив'язки LDAP**

```php
<?php

// используется ldap-привязка
$ldaprdn  = 'uname';     // ldap rdn или dn
$ldappass = 'password';  // ассоциированный пароль

// соединение с сервером
$ldapconn = ldap_connect("ldap://ldap.example.com")
    or die("Не могу соединиться с сервером LDAP.");

if ($ldapconn) {

    // привязка к ldap-серверу
    $ldapbind = ldap_bind($ldapconn, $ldaprdn, $ldappass);

    // проверка привязки
    if ($ldapbind) {
        echo "LDAP-привязка успешна...";
    } else {
        echo "LDAP-привязка не удалась...";
    }

}

?>
```

**Приклад #2 Використання анонімної прив'язки LDAP**

```php
<?php

//анонимное использование ldap-привязки

// соединение с сервером ldap
$ldapconn = ldap_connect("ldap://ldap.example.com")
    or die("Не могу соединиться с сервером LDAP.");

if ($ldapconn) {

    // анонимная привязка
    $ldapbind = ldap_bind($ldapconn);

    if ($ldapbind) {
        echo "Анонимная привязка LDAP прошла успешно...";
    } else {
        echo "Анонимная привязка LDAP не удалась...";
    }

}

?>
```

### Дивіться також

-   [ldapbindext()](function.ldap-bind-ext.html) - Прив'язати до директорії LDAP
-   [ldapunbind()](function.ldap-unbind.html) - Розірвати прив'язку до директорії LDAP