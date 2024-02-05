---
navigation:
  - function.snmp2-getnext.md: « snmp2\_getnext
  - function.snmp2-set.md: snmp2\_set »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp2\_real\_walk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp2\_real\_walk

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2\_real\_walk — Повертає всі об'єкти, включаючи їх ідентифікатор

### Опис

```methodsynopsis
snmp2_real_walk(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функция**snmp2\_real\_walk()** використовується для обходу об'єктів SNMP, починаючи з `object_id` і повертає як їх значення, а й ідентифікатори об'єктів.

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

Повертає асоціативний масив ідентифікаторів об'єктів SNMP та їх значень у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки виводить помилку рівня E\_WARNING.

### Приклади

**Приклад #1 Приклад використання** snmp2\_real\_walk()\*\*\*\*

```php
<?php
 print_r(snmp2_real_walk("localhost", "public", "IF-MIB::ifName"));
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

-   [snmp2\_walk()](function.snmp2-walk.md) \- Отримує всі об'єкти SNMP із агента
