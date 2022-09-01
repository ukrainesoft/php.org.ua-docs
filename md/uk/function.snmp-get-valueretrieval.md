---
navigation:
  - function.snmp-get-quick-print.html: « snmpgetquickprint
  - function.snmp-read-mib.html: snmpreadmib »
  - index.html: PHP Manual
  - ref.snmp.html: Функції SNMP
title: snmpgetvalueretrieval
---
# snmpgetvalueretrieval

(PHP 4> = 4.3.3, PHP 5, PHP 7, PHP 8)

snmpgetvalueretrieval — Повертає метод, як буде повернено значення SNMP

### Опис

```methodsynopsis
snmp_get_valueretrieval(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єднання констант (**`SNMP_VALUE_LIBRARY`** або **`SNMP_VALUE_PLAIN`**) з можливим набором SNMPVALUEOBJECT.

### Приклади

**Приклад #1 Приклад використання **snmpgetvalueretrieval()****

```php
<?php
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 if (snmp_get_valueretrieval() & SNMP_VALUE_OBJECT) {
   echo $ret->value;
 } else {
   echo $ret;
 }
?>
```

### Дивіться також

-   [snmpsetvalueretrieval()](function.snmp-set-valueretrieval.html) - Визначає метод повернення значень SNMP
-   [Обумовлені константи](snmp.constants.html)
