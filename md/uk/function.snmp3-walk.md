---
navigation:
  - function.snmp3-set.md: « snmp3\_set
  - function.snmpget.md: snmpget »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp3\_walk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp3\_walk

(PHP 4, PHP 5, PHP 7, PHP 8)

snmp3\_walk — Отримує всі об'єкти SNMP із агента

### Опис

```methodsynopsis
snmp3_walk(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функция**snmp3\_walk()** використовується для читання всіх значень агента SNMP, зазначеного в `hostname`

Навіть якщо рівень безпеки не використовує протокол авторизації або пароль, необхідно вказати коректні значення.

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

Якщо **`null`** `object_id` береться як корінь дерева об'єктів SNMP і всі об'єкти цього дерева повертаються як масиву.

Якщо вказано `object_id`, повертаються всі об'єкти SNMP нижче цього `object_id`

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає масив значень об'єкта SNMP, починаючи з `object_id` як корінь або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`auth_protocol`тепер приймає`"SHA256"`и`"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Приклад #1 Приклад використання** snmp3\_walk()\*\*\*\*

```php
<?php
$ret = snmp3_walk('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName');
var_export($ret);
?>
```

Виклик функції поверне всі об'єкти SNMP із агента SNMP, запущеного на localhost:

```
array (
  0 => 'STRING: lo',
  1 => 'STRING: eth0',
  2 => 'STRING: eth2',
  3 => 'STRING: sit0',
  4 => 'STRING: sixxs',
)
```

### Дивіться також

-   [snmp3\_real\_walk()](function.snmp3-real-walk.md) \- Повертає всі об'єкти, включаючи їхній ідентифікатор у зазначеному об'єкті
