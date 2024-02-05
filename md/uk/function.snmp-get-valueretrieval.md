---
navigation:
  - function.snmp-get-quick-print.md: « snmp\_get\_quick\_print
  - function.snmp-read-mib.md: snmp\_read\_mib »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp\_get\_valueretrieval
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp\_get\_valueretrieval

(PHP 4 >= 4.3.3, PHP 5, PHP 7, PHP 8)

snmp\_get\_valueretrieval — Повертає метод, як буде повернено значення SNMP

### Опис

```methodsynopsis
snmp_get_valueretrieval(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єднання констант (**`SNMP_VALUE_LIBRARY`**или**`SNMP_VALUE_PLAIN`**) з можливим набором SNMP\_VALUE\_OBJECT.

### Приклади

**Пример #1 Пример использования**snmp\_get\_valueretrieval()\*\*\*\*

```php
<?php
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 if (snmp_get_valueretrieval() & SNMP_VALUE_OBJECT) {
   echo $ret->value;
 } else {
   echo $ret;
 }
?>
```

### Дивіться також

-   [snmp\_set\_valueretrieval()](function.snmp-set-valueretrieval.md) \- Визначає метод повернення значень SNMP
-   [Обумовлені константи](snmp.constants.md)
