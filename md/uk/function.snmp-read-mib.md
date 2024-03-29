---
navigation:
  - function.snmp-get-valueretrieval.md: « snmp\_get\_valueretrieval
  - function.snmp-set-enum-print.md: snmp\_set\_enum\_print »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp\_read\_mib
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp\_read\_mib

(PHP 5, PHP 7, PHP 8)

snmp\_read\_mib - Читає та аналізує файл MIB в активному дереві MIB

### Опис

```methodsynopsis
snmp_read_mib(string $filename): bool
```

Функція використовується для завантаження додаткових, наприклад, специфічних для постачальника, MIB, щоб можна було використовувати легкочитані OID, таких як `VENDOR-MIB::foo.1`, замість схильних до помилок числових OID.

Порядок, в якому завантажуються MIB, має значення, оскільки базова бібліотека Net-SNMP друкуватиме попередження, якщо зазначені об'єкти не можуть бути дозволені.

### Список параметрів

`filename`

Ім'я файлу MIB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** snmp\_read\_mib()\*\*\*\*

```php
<?php

print_r( snmprealwalk('localhost', 'public', '.1.3.6.1.2.1.2.3.4.5') );

snmp_read_mib('./FOO-BAR-MIB.txt');
print_r( snmprealwalk('localhost', 'public', 'FOO-BAR-MIB::someTable') );
?>
```

Наведений вище приклад складено, але результати виглядатимуть так:

```
Array
(
    [iso.3.6.1.2.1.2.3.4.5.0] => Gauge32: 6
)
Array
(
    [FOO-BAR-MIB::someTable.0] => Gauge32: 6
)
```
