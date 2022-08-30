Отримує об'єкт SNMP

-   [« snmpsetvalueretrieval](function.snmp-set-valueretrieval.html)
    
-   [snmp2getnext »](function.snmp2-getnext.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SNMP](ref.snmp.html)
    
-   Отримує об'єкт SNMP
    

# snmp2get

(PHP 5> = 5.2.0, PHP 7, PHP 8)

snmp2get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
snmp2_get(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функція **snmp2get()** використовується для читання значення об'єкта SNMP, вказаного в `object_id`

### Список параметрів

`hostname`

Агент SNMP.

`community`

Read-спільнота.

`object_id`

Об'єкт SNMP.

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **snmp2get()****

```php
<?php
$syscontact = snmp2_get("127.0.0.1", "public", "system.SysContact.0");
?>
```

### Дивіться також

-   [snmp2set()](function.snmp2-set.html) - Встановлює значення об'єкта SNMP