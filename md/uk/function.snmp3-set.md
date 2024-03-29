---
navigation:
  - function.snmp3-real-walk.md: « snmp3\_real\_walk
  - function.snmp3-walk.md: snmp3\_walk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp3\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp3\_set

(PHP 4, PHP 5, PHP 7, PHP 8)

snmp3\_set — Встановлює значення об'єкта SNMP

### Опис

```methodsynopsis
snmp3_set(    string $hostname,    string $security_name,    string $security_level,    string $auth_protocol,    string $auth_passphrase,    string $privacy_protocol,    string $privacy_passphrase,    array|string $object_id,    array|string $type,    array|string $value,    int $timeout = -1,    int $retries = -1): bool
```

Функция**snmp3\_set()** використовується для встановлення значення об'єкта SNMP, зазначеного в `object_id`

Навіть якщо рівень безпеки не використовує протокол авторизації або пароль, необхідно вказати коректні значення.

### Список параметрів

`hostname`

Ім'я хоста агента (сервера) SNMP.

`security_name`

Ім'я безпеки, зазвичай якесь ім'я користувача.

`security_level`

Рівень безпеки (noAuthNoPriv|authNoPriv|authPriv).

`auth_protocol`

Протокол аутентифікації (MD5 чи SHA).

`auth_passphrase`

Пароль для автентифікації.

`privacy_protocol`

Протокол конфіденційності (DES чи AES).

`privacy_passphrase`

Пароль конфіденційності.

`object_id`

Ідентифікатор об'єкта SNMP.

`type`

MIB визначає тип ідентифікатора кожного об'єкта. Він має бути вказаний у вигляді одного символу з наступного списку.

<table class="doctable table"><caption><strong>types</strong></caption><tbody class="tbody"><tr><td>=</td><td>Тип, який приймає MIB</td></tr><tr><td>i</td><td>INTEGER</td></tr><tr><td>u</td><td>INTEGER</td></tr><tr><td>s</td><td>STRING</td></tr><tr><td>x</td><td>HEX STRING</td></tr><tr><td>d</td><td>DECIMAL STRING</td></tr><tr><td>n</td><td>NULLOBJ</td></tr><tr><td>o</td><td>OBJID</td></tr><tr><td>t</td><td>TIMETICKS</td></tr><tr><td>a</td><td>IPADDRESS</td></tr><tr><td>b</td><td>BITS</td></tr></tbody></table>

Якщо при компіляції бібліотеки SNMP було визначено опцію **`OPAQUE_SPECIAL_TYPES`**, то також можуть бути використані такі типи:

<table class="doctable table"><caption><strong>types</strong></caption><tbody class="tbody"><tr><td>U</td><td>unsigned int64</td></tr><tr><td>I</td><td>signed int64</td></tr><tr><td>F</td><td>float</td></tr><tr><td>D</td><td>double</td></tr></tbody></table>

Більшість цих значень використовує очевидний тип ASN.1. 's', 'x', 'd' і 'b' — це різні способи вказівки значення OCTET STRING, а беззнаковий тип 'u' також вказують для обробки значень Gauge32.

Якщо MIB-файли були завантажені в MIB-дерево за допомогою "snmp\_read\_mib" або були вказані в конфігураційному файлі libsnmp, то для вказівки параметра `type` можна використовувати нотацію '=', оскільки тип всіх ідентифікаторів об'єктів буде автоматично зчитаний з MIB.

Зверніть увагу, що є два способи встановити змінну типу BITS, наприклад "SYNTAX BITS {telnet(0), ftp(1), http(2), icmp(3), snmp(4), ssh(5), https( 6)}":

-   За допомогою типу "b" та списку бітових чисел. Не рекомендується використовувати цей метод, тому що GET-запит для того ж OID поверне, наприклад, 0xF8.
-   За допомогою типу "x" та шістнадцяткового числа, але без (!) звичайного префікса "0x".

Докладніше дивіться у розділі з прикладами.

`value`

Нове значення.

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

Якщо хост SNMP відхиляє тип даних, виводиться помилка рівня E\_WARNING на кшталт "Warning: Error in packet. Reason: (badValue) The value given has wrong type or length.". Якщо вказано невідомий або неприпустимий OID, ймовірно, буде виведено попередження "Could not add variable".

### Приклади

**Приклад #1 Приклад використання** snmp3\_set()\*\*\*\*

```php
<?php
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'IF-MIB::ifAlias.3', 's', "foo");
?>
```

**Приклад #2 Приклад використання** snmp3\_set()\*\* для встановлення BITS ідентифікатору об'єкта SNMP\*\*

```php
<?php
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// или
  snmp3_set('localhost', 'james', 'authPriv', 'SHA', 'secret007', 'AES', 'secret007', 'FOO-MIB::bar.42', 'x', 'F0');
?>
```
