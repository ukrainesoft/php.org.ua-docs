---
navigation:
  - function.snmp2-get.md: « snmp2\_get
  - function.snmp2-real-walk.md: snmp2\_real\_walk »
  - index.md: PHP Manual
  - ref.snmp.md: Функції SNMP
title: snmp2\_getnext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# snmp2\_getnext

(PHP >= 5.2.0, PHP 7, PHP 8)

snmp2\_getnext — Отримує об'єкт SNMP, який слідує за цим ідентифікатором об'єкта

### Опис

```methodsynopsis
snmp2_getnext(    string $hostname,    string $community,    array|string $object_id,    int $timeout = -1,    int $retries = -1): mixed
```

Функция**snmp2\_get\_next()** використовується для читання значення об'єкта SNMP, який слідує за вказаним `object_id`

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

**Пример #1 Пример использования**snmp2\_get\_next()\*\*\*\*

```php
<?php
$nameOfSecondInterface = snmp2_get_next('localhost', 'public', 'IF-MIB::ifName.1');
?>
```

### Дивіться також

-   [snmp2\_get()](function.snmp2-get.md) \- Отримує об'єкт SNMP
-   [snmp2\_walk()](function.snmp2-walk.md) \- Отримує всі об'єкти SNMP із агента
