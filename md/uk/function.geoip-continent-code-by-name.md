---
navigation:
  - function.geoip-asnum-by-name.md: « geoip\_asnum\_by\_name
  - function.geoip-country-code-by-name.md: geoip\_country\_code\_by\_name »
  - index.md: PHP Manual
  - ref.geoip.md: Функції GeoIP
title: geoip\_continent\_code\_by\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# geoip\_continent\_code\_by\_name

(PECL geoip >= 1.0.3)

geoip\_continent\_code\_by\_name — Отримати двосимвольний код континенту

### Опис

```methodsynopsis
geoip_continent_code_by_name(string $hostname): string
```

Функция**geoip\_continent\_code\_by\_name()** повертає двосимвольний код континенту, який відповідає імені хоста або IP-адреси.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса, за якою вестиметься пошук.

### Значення, що повертаються

Повертає два символи, що містять код континенту, при знаходженні адреси в базі даних, інакше **`false`**

**Константи кодів**

| Код | Имя континента |
| --- | --- |
| `AF` | Африка |
| `AN` | Антарктика |
| `AS` | Азія |
| `EU` | Європа |
| `NA` | Північна Америка |
| `OC` | Океанія |
| `SA` | Південна Америка |

### Приклади

**Пример #1 Пример использования**geoip\_continent\_code\_by\_name()\*\*\*\*

Цей приклад виведе розташування хоста example.com.

```php
<?php
$continent = geoip_continent_code_by_name('www.example.com');
if ($continent) {
    echo 'Данный хост расположен в ' . $continent;
}
?>
```

Результат виконання наведеного прикладу:

```
Данный хост расположен в NA
```

### Дивіться також

-   [geoip\_country\_code\_by\_name()](function.geoip-country-code-by-name.md) \- Отримати двосимвольний код країни
