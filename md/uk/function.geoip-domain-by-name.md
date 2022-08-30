Отримати ім'я домену другого рівня

-   [« geoipдбgetallinfo](function.geoip-db-get-all-info.html)
    
-   [geoipідбname »](function.geoip-id-by-name.html)
    
-   [PHP Manual](index.md)
    
-   [Функции GeoIP](ref.geoip.md)
    
-   Отримати ім'я домену другого рівня
    

# geoipdomainбname

(PECL geoip >= 1.1.0)

geoipdomainбname — Отримати назву домену другого рівня

### Опис

```methodsynopsis
geoip_domain_by_name(string $hostname): string
```

Функція **geoipdomainбname()** повертає домени другого рівня, пов'язані з ім'ям хоста або IP-адресою.

Зараз ця функція доступна лише користувачам, які купили комерційну версію GeoIP Domain Edition. Якщо коректна база даних не буде знайдена, буде виведено попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання повертає ім'я домену. Якщо адреса не знайдена в базі, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipdomainбname()****

Знайдемо домен, пов'язаний із IP 61.106.139.1.

```php
<?php
$domain = geoip_domain_by_name('61.106.139.1');

if ($domain) {
    echo 'Домен: '. $domain;
}

?>
```

Результат виконання цього прикладу:

```
Домен: von.co.kr
```