Отримує всі об'єкти SNMP з агента

-   [« snmp2set](function.snmp2-set.html)
    
-   [snmpv3get »](function.snmp3-get.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SNMP](ref.snmp.html)
    
-   Отримує всі об'єкти SNMP з агента
    

# snmp2walk

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2walk — Отримує всі об'єкти SNMP із агента

### Опис

```methodsynopsis
snmp2_walk(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функція **snmp2walk()** використовується для читання всіх значень агента SNMP, зазначеного в `hostname`

### Список параметрів

`hostname`

Агент SNMP (сервер).

`community`

Read-спільнота.

`object_id`

Якщо **`null`** `object_id` береться як корінь дерева об'єктів SNMP і всі об'єкти цього дерева повертаються як масиву.

Якщо вказано `object_id`, повертаються всі об'єкти SNMP нижче цього `object_id`

`timeout`

Час очікування у мікросекундах.

`retries`

Кількість повторних спроб після закінчення часу очікування.

### Значення, що повертаються

Повертає масив значень об'єкта SNMP, починаючи з `object_id` як корінь або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **snmp2walk()****

```php
<?php
$a = snmp2_walk("127.0.0.1", "public", "");

foreach ($a as $val) {
    echo "$val\n";
}

?>
```

Виклик функції поверне всі об'єкти SNMP із агента SNMP, що працює на localhost. Можна переміщуватись за значеннями за допомогою циклу.

### Дивіться також

-   [snmp2realwalk()](function.snmp2-real-walk.html) - Повертає всі об'єкти, включаючи їхній ідентифікатор