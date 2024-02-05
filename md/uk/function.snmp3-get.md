---
navigation:
  - function.snmp2-walk.md: « snmp2\_walk
  - function.snmp3-getnext.md: snmp3\_getnext »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp3\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp3\_get

(PHP 4, PHP 5, PHP 7, PHP 8)

snmp3\_get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
snmp3_get(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmp3\_get()** використовується для читання значення об'єкта SNMP, вказаного в `object_id`

### Список параметрів

`hostname`

Ім'я хоста агента (сервера) SNMP.

`security_name`

Ім'я безпеки, зазвичай якесь ім'я користувача.

`security_level`

Рівень безпеки (noAuthNoPriv|authNoPriv|authPriv).

`auth_protocol`

Протокол аутентифікації (`"MD5"` `"SHA"` `"SHA256"`или`"SHA512"`

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

Повертає значення об'єкта SNMP у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`auth_protocol`тепер приймає`"SHA256"`и`"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Пример #1 Пример использования**snmp3\_get()\*\*\*\*

```php
<?php
$nameOfSecondInterface = snmp3_get('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.2');
?>
```

### Дивіться також

-   [snmp3\_set()](function.snmp3-set.md) \- Встановлює значення об'єкта SNMP
