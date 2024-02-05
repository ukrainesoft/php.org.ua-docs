---
navigation:
  - function.snmp3-get.md: « snmp3\_get
  - function.snmp3-real-walk.md: snmp3\_real\_walk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp3\_getnext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp3\_getnext

(PHP 5, PHP 7, PHP 8)

snmp3\_getnext — Отримує об'єкт SNMP, який слідує за вказаним ідентифікатором об'єкта

### Опис

```methodsynopsis
snmp3_getnext(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmp3\_getnext()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

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

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки. У разі помилки виводить помилку рівня E\_WARNING.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`auth_protocol`тепер приймає`"SHA256"`и`"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Пример #1 Пример использования**snmp3\_getnext()\*\*\*\*

```php
<?php
$nameOfSecondInterface = snmp3_getnext('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmp3\_get()](function.snmp3-get.md) \- Отримує об'єкт SNMP
-   [snmp3\_walk()](function.snmp3-walk.md) \- Отримує всі об'єкти SNMP із агента
