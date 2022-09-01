---
navigation:
  - function.snmp-set-quick-print.html: « snmpsetquickprint
  - function.snmp2-get.html: snmp2get »
  - index.html: PHP Manual
  - ref.snmp.html: Функції SNMP
title: snmpsetvalueretrieval
---
# snmpsetvalueretrieval

(PHP 4> = 4.3.3, PHP 5, PHP 7, PHP 8)

snmpsetvalueretrieval — Визначає спосіб повернення значень SNMP

### Опис

```methodsynopsis
snmp_set_valueretrieval(int $method): bool
```

### Список параметрів

`method`

<table class="doctable table"><caption><strong>Типи</strong></caption><tbody class="tbody"><tr><td>SNMP_VALUE_LIBRARY</td><td>Повертані значення будуть такими ж, як повертаються бібліотекою Net-SNMP.</td></tr><tr><td>SNMP_VALUE_OBJECT</td><td>Повертані значення будуть об'єктами з властивостями <code class="literal">value</code> and <code class="literal">type</code>, де останнє є однією з констант <strong><code>SNMP_OCTET_STR</code></strong>, <strong><code>SNMP_COUNTER</code></strong> і т.д. Спосіб повернення <code class="literal">value</code> залежить від того, яка з констант <strong><code>SNMP_VALUE_LIBRARY</code></strong>, <strong><code>SNMP_VALUE_PLAIN</code>&lt; /strong&gt; встановлено.</strong></td></tr></tbody></table>

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **snmpsetvalueretrieval()****

```php
<?php
 snmp_set_valueretrieval(SNMP_VALUE_LIBRARY);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // $ret = "STRING: lo"

 snmp_set_valueretrieval(SNMP_VALUE_PLAIN);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // $ret = "lo";

 snmp_set_valueretrieval(SNMP_VALUE_OBJECT);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, смотрите константы
 //   [value] => lo
 // )

 snmp_set_valueretrieval(SNMP_VALUE_OBJECT | SNMP_VALUE_PLAIN);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, смотрите константы
 //   [value] => lo
 // )

 snmp_set_valueretrieval(SNMP_VALUE_OBJECT | SNMP_VALUE_LIBRARY);
 $ret = snmpget('localhost', 'public', 'IF-MIB::ifName.1');
 // stdClass Object
 // (
 //   [type] => 4        <-- SNMP_OCTET_STR, смотрите константы
 //   [value] => STRING: lo
 // )

?>
```

### Дивіться також

-   [snmpgetvalueretrieval()](function.snmp-get-valueretrieval.html) - Повертає метод, як буде повернено значення SNMP
-   [Обумовлені константи](snmp.constants.html)
