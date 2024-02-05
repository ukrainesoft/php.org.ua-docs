---
navigation:
  - function.snmp-read-mib.md: « snmp\_read\_mib
  - function.snmp-set-oid-numeric-print.md: snmp\_set\_oid\_numeric\_print »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp\_set\_enum\_print
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp\_set\_enum\_print

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

snmp\_set\_enum\_print — Повертає всі значення, які є перерахуваннями, зі значенням їх перерахування замість необробленого цілого числа

### Опис

```methodsynopsis
snmp_set_enum_print(bool $enable): true
```

Функція перемикає, якщо snmpwalk/snmpget тощо. повинні автоматично шукати значення перерахування в MIB і повертати їх разом з їх рядком, що легко читається.

### Список параметрів

`enable`

Оскільки значення інтерпретується бібліотекою Net-SNMP як логічне значення, воно може бути лише "0" або "1".

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

**Приклад #1 Приклад використання** snmp\_set\_enum\_print()\*\*\*\*

```php
<?php
 snmp_set_enum_print(0);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
 snmp_set_enum_print(1);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
?>
```

Приклад вище повинен повернути:

```
INTEGER: up(1)
 INTEGER: 1
```
