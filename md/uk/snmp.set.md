Встановлює значення об'єкта SNMP

-   [« SNMP::getnext](snmp.getnext.html)
    
-   [SNMP::setSecurity »](snmp.setsecurity.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](class.snmp.html)
    
-   Встановлює значення об'єкта SNMP
    

# SNMP::set

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SNMP::set — Встановлює значення об'єкта SNMP

### Опис

```methodsynopsis
public SNMP::set(array|string $objectId, array|string $type, array|string $value): bool
```

Запитує віддалений агент SNMP, що встановлює значення одного або декількох об'єктів SNMP, зазначених у `objectId`

### Список параметрів

Якщо `objectId` - це рядок (string), обидва `type` і `value` також мають бути рядками (string). Якщо `objectId` - масив (array), `value` повинен бути масивом рівного розміру, що містить відповідні значення, `type` може бути рядком (string) (це значення буде використовуватися для всіх пар `objectId``value`) або масив рівного розміру з кожним значенням OID. Коли використовуються комбінації будь-яких інших параметрів, може відображатись ряд повідомлень EWARNING із докладним описом.

`objectId`

Ідентифікатор об'єкта SNMP

Коли кількість OID у масиві objectid більше, ніж maxoids, метод набору властивостей об'єкта повинен використовувати кілька запитів для виконання запрошених оновлень значень. У цьому випадку перевірки типу та значення виконуються для кожного фрагмента, тому другий або наступні запити можуть завершитися помилкою через неправильний тип або значення запитаного OID. Щоб повідомити про це, з'являється попередження, коли кількість OID у масиві objectid перевищує maxoids.

`type`

MIB визначає тип ідентифікатора кожного об'єкта. Він має бути вказаний у вигляді одного символу з наступного списку.

<table class="doctable table"><caption><strong>types</strong></caption><tbody class="tbody"><tr><td>=</td><td>Тип, який приймає MIB</td></tr><tr><td>i</td><td>INTEGER</td></tr><tr><td>u</td><td>INTEGER</td></tr><tr><td>s</td><td>STRING</td></tr><tr><td>x</td><td>HEX STRING</td></tr><tr><td>d</td><td>DECIMAL STRING</td></tr><tr><td>n</td><td>NULLOBJ</td></tr><tr><td>o</td><td>OBJID</td></tr><tr><td>t</td><td>TIMETICKS</td></tr><tr><td>a</td><td>IPADDRESS</td></tr><tr><td>b</td><td>BITS</td></tr></tbody></table>

Якщо при компіляції бібліотеки SNMP було визначено опцію **`OPAQUE_SPECIAL_TYPES`**, то також можуть бути використані такі типи:

< /tr>

<table class="doctable table"><caption><strong>types</strong></caption><tbody class="tbody"><tr><td>U</td><td>unsigned int64</td></tr><tr><td>I</td><td>signed int64</td></tr><tr><td>F</td><td>float</td></tr><tr><td>D</td><td>double</td></tr></tbody></table>

Більшість цих значень використовують явний тип ASN.1. 's', 'x', 'd' та 'b' - це всі різні способи вказівки значення OCTET STRING, а беззнаковий тип 'u' також використовується для обробки значень Gauge32.

Якщо MIB-файли були завантажені в MIB-дерево за допомогою "snmpreadmib" або були вказані в конфігураційному файлі libsnmp, то для вказівки параметра `type` можна використовувати нотацію '=', т.к. тип всіх ідентифікаторів об'єктів буде автоматично зчитаний з MIB.

Зверніть увагу, що є два способи встановити змінну типу BITS, наприклад "SYNTAX BITS {telnet(0), ftp(1), http(2), icmp(3), snmp(4), ssh(5), https( 6)}":

-   За допомогою типу "b" та списку бітових чисел. Не рекомендується використовувати цей спосіб, т.к. GET-запит того ж OID поверне, наприклад, 0xF8.
-   За допомогою типу "x" та шістнадцяткового числа, але без (!) звичайного префікса "0x".

Докладніше дивіться у розділі з прикладами.

`value`

Нове значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Цей метод за промовчанням не генерує винятку. Щоб увімкнути генерацію виключення SNMPException при виникненні деяких помилок цієї бібліотеки, необхідно встановити параметр `exceptions_enabled` класу SNMP у відповідне значення. Детальніше дивіться [объяснении параметра `SNMP::$exceptions_enabled`](class.snmp.html#snmp.props.exceptions-enabled)

### Приклади

**Приклад #1 Встановити одиночний ідентифікатор об'єкта SNMP**

```php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set('SNMPv2-MIB::sysContact.0', 's', "Nobody");
?>
```

**Приклад #2 Встановити кілька значень за допомогою одного дзвінка **SNMP::set()****

```php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set(array('SNMPv2-MIB::sysContact.0', 'SNMPv2-MIB::sysLocation.0'), array('s', 's'), array("Nobody", "Nowhere"));
// или
  $session->set(array('SNMPv2-MIB::sysContact.0', 'SNMPv2-MIB::sysLocation.0'), 's', array("Nobody", "Nowhere"));
?>
```

**Приклад #3 Використання **SNMP::set()** для встановлення ідентифікатора об'єкта BITS SNMP**

```php
<?php
  $session = new SNMP(SNMP::VERSION_2C, "127.0.0.1", "private");
  $session->set('FOO-MIB::bar.42', 'b', '0 1 2 3 4');
// или
  $session->set('FOO-MIB::bar.42', 'x', 'F0');
?>
```

### Дивіться також

-   [SNMP::get()](snmp.get.html) - Отримує об'єкт SNMP