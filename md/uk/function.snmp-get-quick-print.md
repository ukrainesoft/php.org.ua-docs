---
navigation:
  - ref.snmp.md: « Функції SNMP
  - function.snmp-get-valueretrieval.md: snmpgetvalueretrieval »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpgetquickprint
---
# snmpgetquickprint

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpgetquickprint — Отримує поточне значення quickprint бібліотеки NET-SNMP

### Опис

```methodsynopsis
snmp_get_quick_print(): bool
```

Повертає поточне значення, що зберігається в бібліотеці NET-SNMP для quickprint. quickprint за замовчуванням вимкнено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо quickprint включений або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **snmpgetquickprint()****

```php
<?php
$quickprint = snmp_get_quick_print();
?>
```

### Дивіться також

-   [snmpsetquickprint()](function.snmp-set-quick-print.md) - Встановлює значення enable у бібліотеці NET-SNMP для повного опису того, що робить quickprint.
