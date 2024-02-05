---
navigation:
  - snmp.geterror.md: '« SNMP::getError'
  - snmp.set.md: 'SNMP::set »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::getnext'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SNMP::getnext

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SNMP::getnext — Отримати об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

### Опис

```methodsynopsis
public SNMP::getnext(array|string $objectId): mixed
```

Отримайте об'єкт SNMP, який слідує за вказаним `objectId`

### Список параметрів

Якщо `objectId` є рядком, тоді **SNMP::getnext()** поверне об'єкт SNMP у вигляді рядка. Якщо `objectId` є масивом, всі запитані об'єкти SNMP будуть повернуті як асоціативний масив ідентифікаторів об'єктів SNMP та їх значень.

`objectId`

Об'єкт SNMP (OID) або об'єкти

### Значення, що повертаються

Повертає запитані об'єкти SNMP у вигляді рядка або масиву залежно від типу `objectId`или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Цей метод за промовчанням не генерує виняток. Щоб увімкнути генерацію виключення SNMPException при виникненні деяких помилок цієї бібліотеки, необхідно встановити параметр `exceptions_enabled`класса SNMP в соответствующее значение. Подробнее смотрите в[поясненні параметра `SNMP::$exceptions_enabled`](class.snmp.md#snmp.props.exceptions-enabled)

### Приклади

**Приклад #1 Одиночний об'єкт SNMP**

Одиночний об'єкт SNMP може бути запитаний двома способами: як рядкове значення, що повертається, або як одноелементний масив з асоціативним масивом як висновок.

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $nsysdescr = $session->getnext("sysDescr.0");
  echo "$nsysdescr\n";
  $nsysdescr = $session->getnext(array("sysDescr.0"));
  print_r($nsysdescr);
?>
```

Висновок наведеного прикладу буде схожим на:

```
OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
Array
(
    [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
)
```

**Приклад #2 Множинні об'єкти SNMP**

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $results = $session->getnext(array("sysDescr.0", "sysName.0"));
  print_r($results);
  $session->close();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
    [SNMPv2-MIB::sysLocation.0] => STRING: Nowhere
)
```

### Дивіться також

-   [SNMP::getErrno()](snmp.geterrno.md) \- Отримує код останньої помилки
-   [SNMP::getError()](snmp.geterror.md) \- Отримує останнє повідомлення про помилку
