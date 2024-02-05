---
navigation:
  - function.ldap-bind-ext.md: « ldap\_bind\_ext
  - function.ldap-close.md: ldap\_close »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_bind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_bind

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_bind — Прив'язати до LDAP директорії

### Опис

```methodsynopsis
ldap_bind(LDAP\Connection $ldap, ?string $dn = null, ?string $password = null): bool
```

Зв'язує LDAP-директорію із зазначеним RDN та паролем.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

`password`

Якщо `password` не визначено, то буде спроба анонімної прив'язки. Також для анонімної прив'язки можна залишити порожнім `dn`, как определено в[https://tools.ietf.org/html/rfc2251#section-4.2.2](https://tools.ietf.org/html/rfc2251#section-4.2.2)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Приклади

**Приклад #1 Приклад використання прив'язки LDAP**

```php
<?php

// используется ldap-привязка
$ldaprdn  = 'uname';     // ldap rdn или dn
$ldappass = 'password';  // ассоциированный пароль

// соединение с сервером
$ldapconn = ldap_connect("ldap://ldap.example.com")
    or die("Не могу соединиться с сервером LDAP.");

if ($ldapconn) {

    // привязка к ldap-серверу
    $ldapbind = ldap_bind($ldapconn, $ldaprdn, $ldappass);

    // проверка привязки
    if ($ldapbind) {
        echo "LDAP-привязка успешна...";
    } else {
        echo "LDAP-привязка не удалась...";
    }

}

?>
```

**Приклад #2 Використання анонімної прив'язки LDAP**

```php
<?php

//анонимное использование ldap-привязки

// соединение с сервером ldap
$ldapconn = ldap_connect("ldap://ldap.example.com")
    or die("Не могу соединиться с сервером LDAP.");

if ($ldapconn) {

    // анонимная привязка
    $ldapbind = ldap_bind($ldapconn);

    if ($ldapbind) {
        echo "Анонимная привязка LDAP прошла успешно...";
    } else {
        echo "Анонимная привязка LDAP не удалась...";
    }

}

?>
```

### Дивіться також

-   [ldap\_bind\_ext()](function.ldap-bind-ext.md) \- Прив'язати до директорії LDAP
-   [ldap\_unbind()](function.ldap-unbind.md) \- Розірвати прив'язку до директорії LDAP
