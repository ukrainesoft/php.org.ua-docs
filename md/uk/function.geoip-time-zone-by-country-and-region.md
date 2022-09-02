---
navigation:
  - function.geoip-setup-custom-directory.md: « geoipsetupcustomdirectory
  - book.fann.md: FANN »
  - index.md: PHP Manual
  - ref.geoip.md: Функции GeoIP
title: geoiptimezoneбcountryandregion
---
# geoiptimezoneбcountryandregion

(PECL geoip >= 1.0.4)

geoiptimezoneбcountryandregion — Повертає часовий пояс для коду країни та регіону.

### Опис

```methodsynopsis
geoip_time_zone_by_country_and_region(string $country_code, string $region_code = ?): string
```

Функція **geoiptimezoneбcountryandregion()** поверне часовий пояс та код регіону відповідної країни.

У США код регіону відповідає дволітерному скороченню кожного штату. У Канаді код регіону відповідає дволітерному скороченню провінції або територіальний код, який відповідає канадській пошті.

Для решти світу, для представлення регіонів GeoIP використовує коди FIPS 10-4. Ви можете переглянути [» http://www.maxmind.com/app/fips10](http://www.maxmind.com/app/fips10_4) для отримання повного переліку FIPS 10-4 кодів.

Ця функція завжди доступна під час використання бібліотеки GeoIP версії 1.4.1 або новішої. Дані беруться безпосередньо з бібліотеки GeoIP, а не з будь-якої бази даних.

### Список параметрів

`country_code`

Дволітерний код країни (дивіться [geoipcountrycodeбname()](function.geoip-country-code-by-name.md)

`region_code`

Дволітерний (або цифровий) код регіону (дивіться [geoipregionбname()](function.geoip-region-by-name.md)

### Значення, що повертаються

Повертає часовий пояс у разі успішного виконання або **`false`**, якщо країна і одночасно код регіону не можуть бути знайдені.

### Приклади

**Приклад #1 Приклад використання **geoiptimezoneбcountryandregion()** для коду регіону US/Canada**

Надрукує часовий пояс країни CA (Канада), регіону QC (Квебек).

```php
<?php
$timezone = geoip_time_zone_by_country_and_region('CA', 'QC');
if ($timezone) {
    echo 'Часовой пояс для CA/QC: ' . $timezone;
}
?>
```

Результат виконання цього прикладу:

```
Часовой пояс для CA/QC: America/Montreal
```

**Приклад #2 Використання **geoiptimezoneбcountryandregion()**, використовуючи коди FIPS**

Виводить часовий пояс для країни JP (Японія), регіон 01 (Aichi).

```php
<?php
$timezone = geoip_time_zone_by_country_and_region('JP', '01');
if ($timezone) {
    echo 'Часовой пояс для JP/01: ' . $timezone;
}
?>
```

Результат виконання цього прикладу:

```
Часовой пояс для JP/01: Asia/Tokyo
```
