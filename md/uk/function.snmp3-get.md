Отримує об'єкт SNMP

-   [« snmp2\_walk](function.snmp2-walk.html)
    
-   [snmp3\_getnext »](function.snmp3-getnext.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SNMP](ref.snmp.html)
    
-   Отримує об'єкт SNMP
    

# snmpv3get

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpv3get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
snmp3_get(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функція **snmpv3get()** використовується для читання значення об'єкта SNMP, вказаного в `object_id`

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

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                     |
|--------|----------------------------------------------------------------------------------------------|
|        | Параметр `auth_protocol` тепер приймає `"SHA256"` і `"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Приклад #1 Приклад використання **snmpv3get()****

```php
<?php
$nameOfSecondInterface = snmp3_get('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.2');
?>
```

### Дивіться також

-   [snmp3\_set()](function.snmp3-set.html) - Встановлює значення об'єкта SNMP