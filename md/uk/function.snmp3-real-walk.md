---
navigation:
  - function.snmp3-getnext.md: « snmpv3getnext
  - function.snmp3-set.md: snmpv3set »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpv3realwalk
---
# snmpv3realwalk

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpv3realwalk — Повертає всі об'єкти, включаючи їхній ідентифікатор у вказаному об'єкті

### Опис

```methodsynopsis
snmp3_real_walk(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функція **snmpv3realwalk()** використовується для обходу об'єктів SNMP, починаючи з `object_id` і повертає як їх значення, а й ідентифікатори об'єктів.

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

Пароль автентифікації.

`privacy_protocol`

Протокол конфіденційності (DES або AES).

`privacy_passphrase`

Пароль конфіденційності.

`object_id`

Ідентифікатор об'єкта SNMP.

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає асоціативний масив ідентифікаторів об'єктів SNMP та їх значень у разі успішного виконання або **`false`** у разі виникнення помилки. У разі помилки виводить помилку рівня EWARNING.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `auth_protocol` тепер приймає `"SHA256"` і `"SHA512"`якщо підтримується libnetsnmp. |

### Приклади

**Приклад #1 Приклад використання **snmpv3realwalk()****

```php
<?php
 var_export(snmp3_real_walk('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifName'));
?>
```

Приклад вище виведе щось на кшталт:

```
array (
  'IF-MIB::ifName.1' => 'STRING: lo',
  'IF-MIB::ifName.2' => 'STRING: eth0',
  'IF-MIB::ifName.3' => 'STRING: eth2',
  'IF-MIB::ifName.4' => 'STRING: sit0',
  'IF-MIB::ifName.5' => 'STRING: sixxs',
)
```

### Дивіться також

-   [snmpwalk()](function.snmpwalk.md) - Отримує всі об'єкти SNMP з агента
