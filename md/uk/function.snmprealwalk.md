---
navigation:
  - function.snmpgetnext.html: « snmpgetnext
  - function.snmpset.html: snmpset »
  - index.html: PHP Manual
  - ref.snmp.html: Функції SNMP
title: snmprealwalk
---
# snmprealwalk

(PHP 4, PHP 5, PHP 7, PHP 8)

snmprealwalk — Повертає всі об'єкти, включаючи їхній ідентифікатор

### Опис

```methodsynopsis
snmprealwalk(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функція **snmprealwalk()** використовується для обходу об'єктів SNMP, починаючи з `object_id` і повертає як їх значення, а й їх ідентифікатори об'єктів.

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

**Приклад #1 Приклад використання **snmprealwalk()****

```php
<?php
 print_r(snmprealwalk("localhost", "public", "IF-MIB::ifName"));
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

-   [snmpwalk()](function.snmpwalk.html) - Отримує всі об'єкти SNMP із агента
