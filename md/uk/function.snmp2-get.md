---
navigation:
  - function.snmp-set-valueretrieval.md: « snmp\_set\_valueretrieval
  - function.snmp2-getnext.md: snmp2\_getnext »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp2\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp2\_get

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

snmp2\_get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
snmp2_get(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmp2\_get()** використовується для читання значення об'єкта SNMP, вказаного в `object_id`

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

**Приклад #1 Приклад використання** snmp2\_get()\*\*\*\*

```php
<?php
$syscontact = snmp2_get("127.0.0.1", "public", "system.SysContact.0");
?>
```

### Дивіться також

-   [snmp2\_set()](function.snmp2-set.md) \- Встановлює значення об'єкта SNMP
