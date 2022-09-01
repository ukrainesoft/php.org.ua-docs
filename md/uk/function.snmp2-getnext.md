---
navigation:
  - function.snmp2-get.html: « snmp2get
  - function.snmp2-real-walk.html: snmp2realwalk »
  - index.html: PHP Manual
  - ref.snmp.html: Функції SNMP
title: snmp2getnext
---
# snmp2getnext

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2getnext — Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

### Опис

```methodsynopsis
snmp2_getnext(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функція **snmp2getnext()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

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

Повертає значення об'єкта SNMP у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки виводиться помилка рівня EWARNING.

### Приклади

**Приклад #1 Приклад використання **snmp2getnext()****

```php
<?php
$nameOfSecondInterface = snmp2_get_next('localhost', 'public', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmp2get()](function.snmp2-get.html) - Отримує об'єкт SNMP
-   [snmp2walk()](function.snmp2-walk.html) - Отримує всі об'єкти SNMP з агента
