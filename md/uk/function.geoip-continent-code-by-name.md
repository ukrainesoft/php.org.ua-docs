Отримати двосимвольний код континенту

-   [« geoipasnumбname](function.geoip-asnum-by-name.html)
    
-   [geoipcountrycodeбname »](function.geoip-country-code-by-name.html)
    
-   [PHP Manual](index.md)
    
-   [Функции GeoIP](ref.geoip.md)
    
-   Отримати двосимвольний код континенту
    

# geoipcontinentcodeбname

(PECL geoip >= 1.0.3)

geoipcontinentcodeбname — Отримати двосимвольний код континенту

### Опис

```methodsynopsis
geoip_continent_code_by_name(string $hostname): string
```

Функція **geoipcontinentcodeбname()** повертає двосимвольний код континенту, який відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає два символи, що містять код континенту, при знаходженні адреси в базі даних, інакше **`false`**

**Константи кодів**

| Код  | Имя континента   |
|------|------------------|
| `AF` | Африка           |
| `AN` | Антарктика       |
| `AS` | Азія             |
| `EU` | Європа           |
| `NA` | Північна Америка |
| `OC` | Океанія          |
| `SA` | Південна Америка |

### Приклади

**Приклад #1 Приклад використання **geoipcontinentcodeбname()****

Цей приклад виведе розташування хоста example.com.

```php
<?php
$continent = geoip_continent_code_by_name('www.example.com');
if ($continent) {
    echo 'Данный хост расположен в ' . $continent;
}
?>
```

Результат виконання цього прикладу:

```
Данный хост расположен в NA
```

### Дивіться також

-   [geoipcountrycodeбname()](function.geoip-country-code-by-name.html) - Отримати двосимвольний код країни