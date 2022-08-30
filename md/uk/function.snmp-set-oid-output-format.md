Встановлює вихідний OID

-   [« snmpsetoidnumericprint](function.snmp-set-oid-numeric-print.html)
    
-   [snmpsetquickprint »](function.snmp-set-quick-print.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SNMP](ref.snmp.html)
    
-   Встановлює вихідний OID
    

# snmpsetoidoutputformat

(PHP 5> = 5.2.0, PHP 7, PHP 8)

snmpsetoidoutputformat — Встановлює вихідний формат OID

### Опис

```methodsynopsis
snmp_set_oid_output_format(int $format): bool
```

**snmpsetoidoutputformat()** встановлює повний чи числовий формат виведення.

### Список параметрів

`format`

<table class="doctable table"><caption><strong>OID .1.3.6.1.2.1.1.3.0 представлення для різних значень <code class="parameter">format</code></strong></caption><tbody class="tbody"><tr><td><strong><code>SNMP_OID_OUTPUT_FULL</code></strong></td><td>.iso.org.dod.internet.mgmt.mib- 2.system.sysUpTime.sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_NUMERIC</code></strong></td><td>.1.3.6.1.2.1. 1.3.0</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_MODULE</code></strong></td><td>DISMAN-EVENT-MIB::sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_SUFFIX</code></strong></td><td>sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_UCD</code></strong></td><td>system.sysUpTime.sysUpTimeInstance</td></tr><tr><td><strong><code>SNMP_OID_OUTPUT_NONE</code></strong></td><td>Undefined</td></tr></tbody></table>

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання [snmprealwalk()](function.snmprealwalk.html)**

```php
<?php

 snmp_read_mib("/usr/share/mibs/netsnmp/NET-SNMP-TC");

 // default or SNMP_OID_OUTPUT_MODULE
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );

 snmp_set_oid_output_format(SNMP_OID_OUTPUT_NUMERIC);
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );

 snmp_set_oid_output_format(SNMP_OID_OUTPUT_FULL);
 print_r( snmprealwalk('localhost', 'public', 'RFC1213-MIB::sysObjectID') );
?>
```

Приклад вище повинен повернути:

```
Array
 (
    [RFC1213-MIB::sysObjectID.0] => OID: NET-SNMP-TC::linux
 )
 Array
 (
    [.1.3.6.1.2.1.1.2.0] => OID: .1.3.6.1.4.1.8072.3.2.10
 )
 Array
 (
    [.iso.org.dod.internet.mgmt.mib-2.system.sysObjectID.0] => OID: .iso.org.dod.internet.private.enterprises.netSnmp.netSnmpEnumerations.netSnmpAgentOIDs.linux
 )
```