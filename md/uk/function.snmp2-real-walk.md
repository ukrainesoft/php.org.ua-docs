Повертає всі об'єкти, включаючи їхній ідентифікатор

-   [« snmp2\_getnext](function.snmp2-getnext.html)
    
-   [snmp2\_set »](function.snmp2-set.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SNMP](ref.snmp.html)
    
-   Повертає всі об'єкти, включаючи їхній ідентифікатор
    

# snmp2realwalk

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2realwalk — Повертає всі об'єкти, включаючи їх ідентифікатор

### Опис

```methodsynopsis
snmp2_real_walk(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функція **snmp2realwalk()** використовується для обходу об'єктів SNMP, починаючи з `object_id` і повертає як їх значення, а й ідентифікатори об'єктів.

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

Повертає асоціативний масив ідентифікаторів об'єктів SNMP та їх значень у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки виводить помилку рівня EWARNING.

### Приклади

**Приклад #1 Приклад використання **snmp2realwalk()****

```php
<?php
 print_r(snmp2_real_walk("localhost", "public", "IF-MIB::ifName"));
?>
```

Вищезгаданий приклад виведе щось на кшталт:

```
Array
      (
      [IF-MIB::ifName.1] => STRING: lo
      [IF-MIB::ifName.2] => STRING: eth0
      [IF-MIB::ifName.3] => STRING: eth2
      [IF-MIB::ifName.4] => STRING: sit0
      [IF-MIB::ifName.5] => STRING: sixxs
    )
```

### Дивіться також

-   [snmp2\_walk()](function.snmp2-walk.html) - Отримує всі об'єкти SNMP з агента