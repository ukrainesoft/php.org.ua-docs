---
navigation:
  - function.snmp3-walk.md: « snmp3\_walk
  - function.snmpgetnext.md: snmpgetnext »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpget
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmpget

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpget — Отримує об'єкт SNMP

### Опис

```methodsynopsis
snmpget(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmpget()** використовується для читання значення об'єкта SNMP, вказаного в `object_id`

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

Повертає значення об'єкта SNMP у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** snmpget()\*\*\*\*

```php
<?php
$syscontact = snmpget("127.0.0.1", "public", "system.SysContact.0");
?>
```

### Дивіться також

-   [snmpset()](function.snmpset.md) \- Встановлює значення об'єкта SNMP
