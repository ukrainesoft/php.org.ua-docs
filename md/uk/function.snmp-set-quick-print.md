---
navigation:
  - function.snmp-set-oid-output-format.md: « snmp\_set\_oid\_output\_format
  - function.snmp-set-valueretrieval.md: snmp\_set\_valueretrieval »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp\_set\_quick\_print
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp\_set\_quick\_print

(PHP 4, PHP 5, PHP 7, PHP 8)

snmp\_set\_quick\_print — Устанавливает значение`enable`в библиотеке NET-SNMP

### Опис

```methodsynopsis
snmp_set_quick_print(bool $enable): true
```

Устанавливает значение`enable` у бібліотеці NET-SNMP. Якщо встановлено (1), бібліотека SNMP повертатиме "швидко виведені" значення. Це означає, що виводиться лише значення. Якщо `enable` вимкнено (за замовчуванням), бібліотека NET-SNMP виводить додаткову інформацію, включаючи тип значення (наприклад, IpAddress або OID). Крім того, якщо quick\_print вимкнено, бібліотека виводить додаткові шістнадцяткові значення для всіх рядків із трьох або менше символів.

За промовчанням бібліотека NET-SNMP повертає докладні значення quick\_print використовується для повернення лише значення.

В даний час рядки, як і раніше, повертаються з додатковими лапками, це буде виправлено в пізніших версіях.

### Список параметрів

`enable`

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Приклади

Налаштування quick\_print часто використовується при використанні інформації, що повертається, а не при її відображенні.

**Пример #1 Пример использования**snmp\_set\_quick\_print()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
'Timeticks: (0) 0:00:00.00'
'0:00:00.00'
```

### Дивіться також

-   [snmp\_get\_quick\_print()](function.snmp-get-quick-print.md) \- Отримує поточне значення Quick\_print бібліотеки NET-SNMP
