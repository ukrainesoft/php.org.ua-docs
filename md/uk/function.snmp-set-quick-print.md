---
navigation:
  - function.snmp-set-oid-output-format.md: « snmpsetoidoutputformat
  - function.snmp-set-valueretrieval.md: snmpsetvalueretrieval »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpsetquickprint
---
# snmpsetquickprint

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpsetquickprint — Встановлює значення `enable` у бібліотеці NET-SNMP

### Опис

```methodsynopsis
snmp_set_quick_print(bool $enable): bool
```

Встановлює значення `enable` у бібліотеці NET-SNMP. Якщо встановлено (1), бібліотека SNMP повертатиме "швидко виведені" значення. Це означає, що виводиться лише значення. Якщо `enable` вимкнено (за замовчуванням), бібліотека NET-SNMP виводить додаткову інформацію, включаючи тип значення (наприклад, IpAddress або OID). Крім того, якщо quickprint вимкнено, бібліотека виводить додаткові шістнадцяткові значення для всіх рядків із трьох або менше символів.

За промовчанням бібліотека NET-SNMP повертає докладні значення quickprint використовується для повернення лише значення.

В даний час рядки, як і раніше, повертаються з додатковими лапками, це буде виправлено в пізніших версіях.

### Список параметрів

`enable`

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

Налаштування quickprint часто використовується при використанні інформації, що повертається, а не при її відображенні.

**Приклад #1 Приклад використання **snmpsetquickprint()****

```php
<?php
snmp_set_quick_print(0);
$a = snmpget("127.0.0.1", "public", ".1.3.6.1.2.1.2.2.1.9.1");
echo "$a\n";
snmp_set_quick_print(1);
$a = snmpget("127.0.0.1", "public", ".1.3.6.1.2.1.2.2.1.9.1");
echo "$a\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
'Timeticks: (0) 0:00:00.00'
'0:00:00.00'
```

### Дивіться також

-   [snmpgetquickprint()](function.snmp-get-quick-print.md) - Отримує поточне значення Quickprint бібліотеки NET-SNMP
