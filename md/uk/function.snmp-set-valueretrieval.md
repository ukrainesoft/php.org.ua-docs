- [« snmp_set_quick_print](function.snmp-set-quick-print.md)
- [snmp2_get »](function.snmp2-get.md)

- [PHP Manual](index.md)
- [Функції SNMP](ref.snmp.md)
- Визначає спосіб повернення значень SNMP

#snmp_set_valueretrieval

(PHP 4 \>= 4.3.3, PHP 5, PHP 7, PHP 8)

snmp_set_valueretrieval — Визначає спосіб повернення значень SNMP

### Опис

**snmp_set_valueretrieval**(int `$method`): bool

### Список параметрів

`method`
|                    |                                                                                                                                                                                                                                                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMP_VALUE_LIBRARY | Значення, що повертаються, будуть такими ж, як повертаються бібліотекою Net-SNMP.                                                                                                                                                                                         |
| SNMP_VALUE_PLAIN   | Значення, що повертаються, будуть простими значеннями без інформації про типи SNMP.                                                                                                                                                                                       |
| SNMP_VALUE_OBJECT  | Значення, що повертаються будуть об'єктами з властивостями value and type, де останнє є однією з констант **SNMP_OCTET_STR**, **SNMP_COUNTER** і т.д. Спосіб повернення value залежить від того, яка з констант **SNMP_VALUE_LIBRARY**, **SNMP_VALUE_PLAIN** встановлена. |

**Типи**

### Значення, що повертаються

Функція завжди повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **snmp_set_valueretrieval()****

`<?php snmp_set_valueretrieval(SNMP_VALUE_LIBRARY); $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1'); // $ret = "STRING: lo" snmp_set_valueretrieval(SNMP_VALUE_PLAIN); $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1'); //$$ret=="lo"; snmp_set_valueretrieval(SNMP_VALUE_OBJECT); $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1'); // stdClass Object // ( //   [type] => 4        <-- SNMP_OCTET_STR, дивіться константи //   [value] => lo| $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1'); // stdClass Object // ( //   [type] => 4        <-- SNMP_OCTET_STR, дивіться константи //   [value] => lo| $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1'); // stdClass Object // ( //   [type] => 4        <-- SNMP_OCTET_STR, дивіться константи //   [value] => STRING:

### Дивіться також

- [snmp_get_valueretrieval()](function.snmp-get-valueretrieval.md) -
Повертає метод, як буде повернено значення SNMP
- [Предвизначені константи](snmp.constants.md)
