Отримує поточне значення Quickprint бібліотеки NET-SNMP

-   [« Функції SNMP](ref.snmp.md)
    
-   [snmpgetvalueretrieval »](function.snmp-get-valueretrieval.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SNMP](ref.snmp.md)
    
-   Отримує поточне значення Quickprint бібліотеки NET-SNMP
    

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

-   [snmpsetquickprint()](function.snmp-set-quick-print.html) - Встановлює значення enable у бібліотеці NET-SNMP для повного опису того, що робить quickprint.