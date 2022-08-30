Отримує об'єкт SNMP

-   [« SNMP::construct](snmp.construct.html)
    
-   [SNMP::getErrno »](snmp.geterrno.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](class.snmp.html)
    
-   Отримує об'єкт SNMP
    

# SNMP::get

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::get — Отримує об'єкт SNMP

### Опис

```methodsynopsis
public SNMP::get(array|string $objectId, bool $preserveKeys = false): mixed
```

Отримує об'єкт SNMP, вказаний у `objectId`за допомогою запиту GET.

### Список параметрів

Якщо `objectId` є рядком, то **SNMP::get()** поверне об'єкт SNMP у вигляді рядка. Якщо `objectId` є масивом, всі запитані об'єкти SNMP будуть повернуті як асоціативний масив ідентифікаторів об'єктів SNMP та їх значень.

`objectId`

Об'єкт SNMP (OID) або об'єкти

`preserveKeys`

Коли `objectId` є масивом і для параметра `preserveKeys` встановлено значення **`true`** ключі в результатах будуть взяті так само, як у `objectId`, інакше властивість SNMP::oidoutputformat використовується визначення форми ключів.

### Значення, що повертаються

Повертає запитані об'єкти SNMP у вигляді рядка або масиву залежно від типу `objectId` або **`false`** у разі виникнення помилки.

### Помилки

Цей метод за промовчанням не генерує винятку. Щоб увімкнути генерацію виключення SNMPException при виникненні деяких помилок цієї бібліотеки, необхідно встановити параметр `exceptions_enabled` класу SNMP у відповідне значення. Детальніше дивіться [объяснении параметра`SNMP::$exceptions_enabled`](class.snmp.html#snmp.props.exceptions-enabled)

### Приклади

**Приклад #1 Одиночний об'єкт SNMP**

Одиночний об'єкт SNMP може бути запитаний двома способами: як рядкове значення, що повертається, або як одноелементний масив з асоціативним масивом як висновок.

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $sysdescr = $session->get("sysDescr.0");
  echo "$sysdescr\n";
  $sysdescr = $session->get(array("sysDescr.0"));
  print_r($sysdescr);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
STRING: Test server
Array
(
    [SNMPv2-MIB::sysDescr.0] => STRING: Test server
)
```

**Приклад #2 Множинні об'єкти SNMP**

```php
$session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $results = $session->get(array("sysDescr.0", "sysName.0"));
  print_r($results);
  $session->close();
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [SNMPv2-MIB::sysDescr.0] => STRING: Test server
    [SNMPv2-MIB::sysName.0] => STRING: myhost.nodomain
)
```

### Дивіться також

-   [SNMP::getErrno()](snmp.geterrno.html) - Отримує код останньої помилки
-   [SNMP::getError()](snmp.geterror.html) - Отримує останнє повідомлення про помилку