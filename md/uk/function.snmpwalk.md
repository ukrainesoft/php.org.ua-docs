---
navigation:
  - function.snmpset.md: « snmpset
  - function.snmpwalkoid.md: snmpwalkoid »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpwalk
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmpwalk

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpwalk — Отримує всі об'єкти SNMP із агента

### Опис

```methodsynopsis
snmpwalk(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функция**snmpwalk()** використовується для читання всіх значень агента SNMP, зазначеного в `hostname`

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

Повертає масив значень об'єкта SNMP, починаючи з `object_id` як корінь або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** snmpwalk()\*\*\*\*

```php
<?php
$a = snmpwalk("127.0.0.1", "public", "");

foreach ($a as $val) {
    echo "$val\n";
}

?>
```

Виклик функції поверне всі об'єкти SNMP із агента SNMP, що працює на localhost. Можна переміщуватись за значеннями за допомогою циклу.

### Дивіться також

-   [snmprealwalk()](function.snmprealwalk.md) \- Повертає всі об'єкти, включаючи їхній ідентифікатор
