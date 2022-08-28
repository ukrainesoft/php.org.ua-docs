Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

-   [« snmpget](function.snmpget.html)
    
-   [snmprealwalk »](function.snmprealwalk.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SNMP](ref.snmp.html)
    
-   Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта
    

# snmpgetnext

(PHP 5, PHP 7, PHP 8)

snmpgetnext — Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

### Опис

```methodsynopsis
snmpgetnext(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функція **snmpgetnext()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

### Список параметрів

`hostname`

Ім'я хоста агента (сервера) SNMP.

`community`

Read-спільнота.

`object_id`

Ідентифікатор об'єкта SNMP, який передує бажаному.

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки виводиться помилка рівня EWARNING.

### Приклади

**Приклад #1 Приклад використання **snmpgetnext()****

```php
<?php
$nameOfSecondInterface = snmpgetnetxt('localhost', 'public', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmpget()](function.snmpget.html) - Отримує об'єкт SNMP
-   [snmpwalk()](function.snmpwalk.html) - Отримує всі об'єкти SNMP з агента