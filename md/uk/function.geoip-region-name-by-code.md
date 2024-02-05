---
navigation:
  - function.geoip-region-by-name.md: « geoip\_region\_by\_name
  - function.geoip-setup-custom-directory.md: geoip\_setup\_custom\_directory »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_region\_name\_by\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_region\_name\_by\_code

(PECL geoip >= 1.0.4)

geoip\_region\_name\_by\_code — Повертає назву регіону для вибраної країни та код регіону

### Опис

```methodsynopsis
geoip_region_name_by_code(string $country_code, string $region_code): string
```

Функция**geoip\_region\_name\_by\_code()** повертає назву регіону, відповідної країни та коду регіону.

У США код регіону відповідає дволітерному скороченню кожному штату. У Канаді код регіону відповідає дволітерному скороченню імені провінції чи території, наданий поштовою службою Канади.

Для решти світу GeoIP використовує коди FIPS 10-4 для представлення регіону. Дивіться також [» http://www.maxmind.com/app/fips10\_ 4](http://www.maxmind.com/app/fips10_4) - Докладний список кодів FIPS 10-4.

Ця функція завжди доступна при використанні бібліотеки GeoIP версії 1.4.1 та новішої. Дані беруться безпосередньо з бібліотеки GeoIP, а не з будь-якої бази.

### Список параметрів

`country_code`

Двохлітерний код країни [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md)) .

`region_code`

Дволітерний (або цифровий) код регіону [geoip\_region\_by\_name()](function.geoip-region-by-name.md)) .

### Значення, що повертаються

Возвращает название региона в случае успехе или\*\*`false`\*\*, якщо країна та код регіону не знайдені у базі даних.

### Приклади

**Приклад #1 Приклад використання** geoip\_region\_name\_by\_code()\*\* (Для Канади/США)\*\*

Буде виведено назву регіону країни CA (Канада), регіону QC (Квебек).

```php
<?php
$region = geoip_region_name_by_code('CA', 'QC');
if ($region) {
    echo 'Название региона для CA/QC: ' . $region;
}
?>
```

Результат виконання наведеного прикладу:

```
Название региона для CA/QC: Quebec
```

**Приклад #2 Приклад використання** geoip\_region\_name\_by\_code()**, використовуючи коди FIPS**

Буде виведено ім'я регіону для країни JP (Японія), регіону 01 (префектура Айті).

```php
<?php
$region = geoip_region_name_by_code('JP', '01');
if ($region) {
    echo 'Название региона для JP/01: ' . $region;
}
?>
```

Результат виконання наведеного прикладу:

```
Название региона для JP/01: Aichi
```
