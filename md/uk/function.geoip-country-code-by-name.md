- [« geoip_continent_code_by_name](function.geoip-continent-code-by-name.md)
- [geoip_country_code3_by_name »](function.geoip-country-code3-by-name.md)

- [PHP Manual](index.md)
- [Функції GeoIP](ref.geoip.md)
- Отримати двосимвольний код країни

# geoip_country_code_by_name

(PECL geoip \>= 0.2.0)

geoip_country_code_by_name — Отримати двосимвольний код країни

### Опис

**geoip_country_code_by_name**(string `$hostname`): string

Функція **geoip_country_code_by_name()** повертає двосимвольний код
країни, що відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`
Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає два символи, що містять код країни за ISO 3166-1, при
знаходження адреси в базі даних, інакше **`false`**.

### Приклади

**Приклад #1 Приклад використання **geoip_country_code_by_name()****

Цей приклад виведе розташування хоста example.com.

` <?php$country = geoip_country_code_by_name('www.example.com');if ($country) {    echo 'Хост розташований в ' . $country;}?> `

Результат виконання цього прикладу:

Хост розташований в US

### Примітки

**Застереження**

Будь ласка, ознайомтесь з повним списком допустимих повертаних
значень, у тому числі спеціальних кодів, тут
[»http://www.maxmind.com/en/iso3166](http://www.maxmind.com/en/iso3166).

### Дивіться також

- [geoip_country_code3_by_name()](function.geoip-country-code3-by-name.md) -
Отримати трисимвольний код країни
- [geoip_country_name_by_name()](function.geoip-country-name-by-name.md) -
Отримати повну назву країни
