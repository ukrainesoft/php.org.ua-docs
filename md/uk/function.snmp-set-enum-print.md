Повертає всі значення, які є перерахуваннями, із їх значенням перерахування замість необробленого цілого числа

-   [« snmpreadmib](function.snmp-read-mib.html)
    
-   [snmpsetoidnumericprint »](function.snmp-set-oid-numeric-print.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SNMP](ref.snmp.html)
    
-   Повертає всі значення, які є перерахуваннями, із їх значенням перерахування замість необробленого цілого числа
    

# snmpsetenumprint

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

snmpsetenumprint — Повертає всі значення, які є перерахуваннями, зі значенням їх перерахування замість необробленого цілого числа

### Опис

```methodsynopsis
snmp_set_enum_print(bool $enable): bool
```

Функція перемикає, якщо snmpwalk/snmpget тощо. повинні автоматично шукати значення перерахування в MIB і повертати їх разом з їх рядком, що легко читається.

### Список параметрів

`enable`

Оскільки значення інтерпретується бібліотекою Net-SNMP як логічне значення, воно може бути лише "0" або "1".

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **snmpsetenumprint()****

```php
<?php
 snmp_set_enum_print(0);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
 snmp_set_enum_print(1);
 echo snmpget('localhost', 'public', 'IF-MIB::ifOperStatus.3') . "\n";
?>
```

Приклад вище повинен повернути:

```
INTEGER: up(1)
 INTEGER: 1
```