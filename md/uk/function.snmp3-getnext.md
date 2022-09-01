---
navigation:
  - function.snmp3-get.html: « snmpv3get
  - function.snmp3-real-walk.html: snmpv3realwalk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpv3getnext
---
# snmpv3getnext

(PHP 5, PHP 7, PHP 8)

snmpv3getnext — Отримує об'єкт SNMP, який слідує за вказаним ідентифікатором об'єкта

### Опис

```methodsynopsis
snmp3_getnext(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функція **snmpv3getnext()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

### Список параметрів

`hostname`

Ім'я хоста агента (сервера) SNMP.

`security_name`

Ім'я безпеки, зазвичай якесь ім'я користувача.

`security_level`

Рівень безпеки (noAuthNoPriv|authNoPriv|authPriv).

`auth_protocol`

Протокол аутентифікації (`"MD5"` `"SHA"` `"SHA256"` або `"SHA512"`

`auth_passphrase`

Пароль для автентифікації.

`privacy_protocol`

Протокол конфіденційності (DES чи AES).

`privacy_passphrase`

Пароль конфіденційності.

`object_id`

Ідентифікатор об'єкта SNMP.

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки. У разі помилки виводить помилку рівня EWARNING.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `auth_protocol` тепер приймає `"SHA256"` і `"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Приклад #1 Приклад використання **snmpv3getnext()****

```php
<?php
$nameOfSecondInterface = snmp3_getnext('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmpv3get()](function.snmp3-get.html) - Отримує об'єкт SNMP
-   [snmpv3walk()](function.snmp3-walk.html) - Отримує всі об'єкти SNMP з агента
