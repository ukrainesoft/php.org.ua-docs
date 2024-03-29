---
navigation:
  - function.snmprealwalk.md: « snmprealwalk
  - function.snmpwalk.md: snmpwalk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmpset

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpset — Встановлює значення об'єкта SNMP

### Опис

```methodsynopsis
snmpset(    string $hostname,    string $community,    array|string $object_id,    array|string $type,    array|string $value,    int $timeout = -1,    int $retries = -1): bool
```

**snmpset()** використовується для встановлення значення об'єкта SNMP, вказаного у параметрі `object_id`

### Список параметрів

`hostname`

Ім'я хоста агента (сервера) SNMP.

`community`

Write-спільнота.

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

**Приклад #1 Приклад використання** snmpset()\*\*\*\*

```php
<?php
  snmpset("localhost", "public", "IF-MIB::ifAlias.3", "s", "foo");
?>
```

**Приклад #2 Приклад використання** snmpset()\*\* для встановлення BITS ідентифікатору об'єкта SNMP\*\*

```php
<?php
  snmpset("localhost", "public", 'FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// or
  snmpset("localhost", "public", 'FOO-MIB::bar.42', 'x', 'F0');
?>
```

### Дивіться також

-   [snmpget()](function.snmpget.md) \- Отримує об'єкт SNMP
