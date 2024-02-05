---
navigation:
  - snmp.construct.md: '« SNMP::\_\_construct'
  - snmp.geterrno.md: 'SNMP::getErrno »'
  - index.md: PHP Manual
  - class.snmp.md: SNMP
title: 'SNMP::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SNMP::get

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SNMP::get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
public SNMP::get(array|string $objectId, bool $preserveKeys = false): mixed
```

Отримує об'єкт SNMP, вказаний у `objectId`, за допомогою запиту GET.

### Список параметрів

Якщо `objectId` є рядком, то **SNMP::get()** поверне об'єкт SNMP у вигляді рядка. Якщо `objectId` є масивом, всі запитані об'єкти SNMP будуть повернуті як асоціативний масив ідентифікаторів об'єктів SNMP та їх значень.

`objectId`

Об'єкт SNMP (OID) або об'єкти

`preserveKeys`

Когда`objectId` є масивом і для параметра `preserveKeys`установлено значение\*\*`true`\*\* ключі в результатах будуть взяті так само, як у `objectId`, інакше властивість SNMP::oid\_output\_format використовується визначення форми ключів.

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
  $sysdescr = $session->get("sysDescr.0");
  echo "$sysdescr\n";
  $sysdescr = $session->get(array("sysDescr.0"));
  print_r($sysdescr);
?>
```

Висновок наведеного прикладу буде схожим на:

```
STRING: Test server
Array
(
    [SNMPv2-MIB::sysDescr.0] => STRING: Test server
)
```

**Приклад #2 Множинні об'єкти SNMP**

```php
$session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $results = $session->get(array("sysDescr.0", "sysName.0"));
  print_r($results);
  $session->close();
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [SNMPv2-MIB::sysDescr.0] => STRING: Test server
    [SNMPv2-MIB::sysName.0] => STRING: myhost.nodomain
)
```

### Дивіться також

-   [SNMP::getErrno()](snmp.geterrno.md) \- Отримує код останньої помилки
-   [SNMP::getError()](snmp.geterror.md) \- Отримує останнє повідомлення про помилку
