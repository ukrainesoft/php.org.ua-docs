---
navigation:
  - function.geoip-db-filename.html: « geoipдбfilename
  - function.geoip-domain-by-name.html: geoipdomainбname »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoipдбgetallinfo
---
# geoipдбgetallinfo

(PECL geoip >= 1.0.1)

geoipдбgetallinfo — Повертає детальну інформацію про всі типи бази GeoIP

### Опис

```methodsynopsis
geoip_db_get_all_info(): array
```

Функція **geoipдбgetallinfo()** повертає докладну інформацію про всі типи бази GeoIP у вигляді багатовимірного масиву.

Ця функція доступна навіть за відсутності встановлених баз даних. При цьому типи будуть перераховані та позначені як недоступні.

Імена різних ключів асоціативного масиву, що повертається:

-   "available" -- Логічний тип, чи вказує доступна база (дивіться [geoipдбavail()](function.geoip-db-avail.md)
-   "description" -- Опис бази даних
-   "filename" - Ім'я файлу бази даних на диску (дивіться [geoipдбfilename()](function.geoip-db-filename.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив.

### Приклади

**Приклад #1 Приклад використання **geoipдбgetallinfo()****

Виводить масив, що містить всю інформацію про базу даних.

```php
<?php
$infos = geoip_db_get_all_info();
if (is_array($infos)) {
    var_dump($infos);
}
?>
```

Результат виконання цього прикладу:

```
array(11) {
  [1]=>
  array(3) {
    ["available"]=>
    bool(true)
    ["description"]=>
    string(21) "GeoIP Country Edition"
    ["filename"]=>
    string(32) "/usr/share/GeoIP/GeoIP.dat"
  }

[ ... ]

  [11]=>
  array(3) {
    ["available"]=>
    bool(false)
    ["description"]=>
    string(25) "GeoIP Domain Name Edition"
    ["filename"]=>
    string(38) "/usr/share/GeoIP/GeoIPDomain.dat"
  }
}
```

**Приклад #2 Приклад використання **geoipдбgetallinfo()****

Ви можете використовувати різноманітні константи як ключі для отримання лише конкретної частини інформації.

```php
<?php
$infos = geoip_db_get_all_info();
if ($infos[GEOIP_COUNTRY_EDITION]['available']) {
    echo $infos[GEOIP_COUNTRY_EDITION]['description'];
}
?>
```

Результат виконання цього прикладу:

```
GeoIP Country Edition
```
