Повертає ім'я інтернет-провайдера (ISP)

-   [« geoipідбname](function.geoip-id-by-name.html)
    
-   [geoipnetspeedcellбname »](function.geoip-netspeedcell-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає ім'я інтернет-провайдера (ISP)
    

# geoipispбname

(PECL geoip >= 1.0.2)

geoipispбname — Повертає ім'я інтернет-провайдера (ISP)

### Опис

```methodsynopsis
geoip_isp_by_name(string $hostname): string
```

Функція **geoipispбname()** повертає ім'я інтернет-провайдера (ISP) вказаної IP-адреси.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP ISP. Якщо такої бази немає, виводиться попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

Повертає ім'я ISP у разі успішного виконання або **`false`**, якщо адресу не знайдено у базі даних.

### Приклади

**Приклад #1 Приклад використання **geoipispбname()****

Відобразить ім'я ISP для хоста example.com.

```php
<?php
$isp = geoip_isp_by_name('www.example.com');
if ($isp) {
    echo 'Этот IP-адрес управляется провайдером: ' . $isp;
}
?>
```

Результат виконання цього прикладу:

```
Адрес управляется провайдером: ICANN c/o Internet Assigned Numbers Authority
```