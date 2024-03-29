---
navigation:
  - function.snmp2-real-walk.md: « snmp2\_real\_walk
  - function.snmp2-walk.md: snmp2\_walk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp2\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp2\_set

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2\_set — Встановлює значення об'єкта SNMP

### Опис

```methodsynopsis
snmp2_set(    string $hostname,    string $community,    array|string $object_id,    array|string $type,    array|string $value,    int $timeout = -1,    int $retries = -1): bool
```

**snmp2\_set()** використовується для встановлення значення об'єкта SNMP, зазначеного в `object_id`

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

**Приклад #1 Приклад використання** snmp2\_set()\*\*\*\*

```php
<?php
  snmp2_set("localhost", "public", "IF-MIB::ifAlias.3", "s", "foo");
?>
```

**Приклад #2 Приклад використання** snmp2\_set()\*\* для встановлення BITS ідентифікатору об'єкта SNMP\*\*

```php
<?php
  snmp2_set("localhost", "public", 'FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// или
  snmp2_set("localhost", "public", 'FOO-MIB::bar.42', 'x', 'F0');
?>
```

### Дивіться також

-   [snmp2\_get()](function.snmp2-get.md) \- Отримує об'єкт SNMP
