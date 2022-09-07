---
navigation:
  - function.snmpwalk.md: « snmpwalk
  - class.snmp.md: SNMP »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmpwalkoid
---
# snmpwalkoid

(PHP 4, PHP 5, PHP 7, PHP 8)

snmpwalkoid — Запит дерева інформації про мережевий об'єкт

### Опис

```methodsynopsis
snmpwalkoid(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): array|false
```

Функція **snmpwalkoid()** використовується для читання всіх ідентифікаторів об'єктів та їх відповідних значень агента SNMP, зазначеного в `hostname`

Функції **snmpwalkoid()** і [snmpwalk()](function.snmpwalk.md) існує з історичних причин. Обидві функції призначені для зворотної сумісності. Натомість використовуйте функцію [snmprealwalk()](function.snmprealwalk.md)

### Список параметрів

`hostname`

Агент SNMP.

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

Повертає асоціативний масив з ідентифікаторами об'єктів та відповідними їм значеннями об'єктів, починаючи з `object_id` як корінь або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **snmpwalkoid()****

```php
<?php
$a = snmpwalkoid("127.0.0.1", "public", "");
for (reset($a); $i = key($a); next($a)) {
    echo "$i: $a[$i]<br />\n";
}
?>
```

Виклик функції поверне всі об'єкти SNMP із агента SNMP, що працює на localhost. Можна переміщуватись за значеннями за допомогою циклу.

### Дивіться також

-   [snmpwalk()](function.snmpwalk.md) - Отримує всі об'єкти SNMP із агента
