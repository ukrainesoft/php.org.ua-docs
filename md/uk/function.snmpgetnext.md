---
navigation:
  - function.snmpget.md: « snmpget
  - function.snmprealwalk.md: snmprealwalk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpgetnext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmpgetnext

(PHP 5, PHP 7, PHP 8)

snmpgetnext — Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

### Опис

```methodsynopsis
snmpgetnext(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmpgetnext()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

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

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки виводиться помилка рівня E\_WARNING.

### Приклади

**Приклад #1 Приклад використання** snmpgetnext()\*\*\*\*

```php
<?php
$nameOfSecondInterface = snmpgetnetxt('localhost', 'public', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmpget()](function.snmpget.md) \- Отримує об'єкт SNMP
-   [snmpwalk()](function.snmpwalk.md) \- Отримує всі об'єкти SNMP із агента
