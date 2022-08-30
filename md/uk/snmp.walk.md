Отримує піддерево об'єкта SNMP

-   [« SNMP::setSecurity](snmp.setsecurity.md)
    
-   [SNMPException »](class.snmpexception.md)
    
-   [PHP Manual](index.md)
    
-   [SNMP](class.snmp.md)
    
-   Отримує піддерево об'єкта SNMP
    

# SNMP::walk

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::walk — Отримує піддерево об'єкта SNMP

### Опис

```methodsynopsis
public SNMP::walk(    array|string $objectId,    bool $suffixAsKey = false,    int $maxRepetitions = -1,    int $nonRepeaters = -1): array|false
```

**SNMP::walk()** використовується для читання піддерева SNMP з коренем у вказаному `objectId`

### Список параметрів

`objectId`

Корінь видобутого піддерева

`suffixAsKey`

За промовчанням для ключів у вихідному масиві використовується повна нотація OID. Якщо встановлено значення **`true`**, префікс піддерева буде видалено з ключів, залишиться тільки суфікс objectid.

`nonRepeaters`

Визначає кількість наданих змінних, які слід повторювати. За замовчуванням використовується значення об'єкта SNMP.

`maxRepetitions`

Визначає максимальну кількість ітерацій за змінними, що повторюються. За замовчуванням використовується значення об'єкта SNMP.

### Значення, що повертаються

Повертає асоціативний масив ідентифікаторів об'єктів SNMP та їх значень у разі успішного виконання або **`false`** у разі виникнення помилки. Коли виникає помилка SNMP, [SNMP::getErrno()](snmp.geterrno.md) і [SNMP::getError()](snmp.geterror.md) можуть використовуватися для отримання номера помилки (специфічно для модуля SNMP, дивіться константи класу) та повідомлення про помилку відповідно.

### Помилки

Цей метод за промовчанням не генерує винятку. Щоб увімкнути генерацію виключення SNMPException при виникненні деяких помилок цієї бібліотеки, необхідно встановити параметр `exceptions_enabled` класу SNMP у відповідне значення. Детальніше дивіться [поясненні параметра`SNMP::$exceptions_enabled`](class.snmp.html#snmp.props.exceptions-enabled)

### Приклади

**Приклад #1 Приклад використання **SNMP::walk()****

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $fulltree = $session->walk(".");
  print_r($fulltree);
  $session->close();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [SNMPv2-MIB::sysDescr.0] => STRING: Test server
    [SNMPv2-MIB::sysObjectID.0] => OID: NET-SNMP-MIB::netSnmpAgentOIDs.8
    [DISMAN-EVENT-MIB::sysUpTimeInstance] => Timeticks: (1150681750) 133 days, 4:20:17.50
    [SNMPv2-MIB::sysContact.0] => STRING: Nobody
    [SNMPv2-MIB::sysName.0] => STRING: server.localdomain
    ...
)
```

**Приклад #2 Приклад використання `suffixAsKey`**

`suffixAsKey` може використовуватися при об'єднанні декількох піддерев SNMP в одне. У цьому вся прикладі імена інтерфейсів зіставляються зі своїми типом.

```php
<?php
  $session = new SNMP(SNMP::VERSION_1, "127.0.0.1", "public");
  $session->valueretrieval = SNMP_VALUE_PLAIN;
  $ifDescr = $session->walk(".1.3.6.1.2.1.2.2.1.2", TRUE);
  $session->valueretrieval = SNMP_VALUE_LIBRARY;
  $ifType = $session->walk(".1.3.6.1.2.1.2.2.1.3", TRUE);
  print_r($ifDescr);
  print_r($ifType);
  $result = array();
  foreach($ifDescr as $i => $n) {
    $result[$n] = $ifType[$i];
  }
  print_r($result);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [1] => igb0
    [2] => igb1
    [3] => ipfw0
    [4] => lo0
    [5] => lagg0
)
Array
(
    [1] => INTEGER: ieee8023adLag(161)
    [2] => INTEGER: ieee8023adLag(161)
    [3] => INTEGER: ethernetCsmacd(6)
    [4] => INTEGER: softwareLoopback(24)
    [5] => INTEGER: ethernetCsmacd(6)
)
Array
(
    [igb0] => INTEGER: ieee8023adLag(161)
    [igb1] => INTEGER: ieee8023adLag(161)
    [ipfw0] => INTEGER: ethernetCsmacd(6)
    [lo0] => INTEGER: softwareLoopback(24)
    [lagg0] => INTEGER: ethernetCsmacd(6)
)
```

### Дивіться також

-   [SNMP::getErrno()](snmp.geterrno.md) - Отримує код останньої помилки
-   [SNMP::getError()](snmp.geterror.md) - Отримує останнє повідомлення про помилку