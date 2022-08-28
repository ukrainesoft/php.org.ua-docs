Повертає назву організації, яка володіє IP-адресою

-   [« geoip\_netspeedcell\_by\_name](function.geoip-netspeedcell-by-name.html)
    
-   [geoip\_record\_by\_name »](function.geoip-record-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Повертає назву організації, яка володіє IP-адресою
    

# geoiporgбname

(PECL geoip >= 0.2.0)

geoiporgбname — Повертає назву організації, яка володіє IP-адресою

### Опис

```methodsynopsis
geoip_org_by_name(string $hostname): string
```

Функція **geoiporgбname()** повертає назву організації, яка володіє вказаною IP-адресою.

Ця функція доступна лише для тих, хто придбав комерційну версію GeoIP Organization, ISP або AS. Якщо такої бази немає, виводиться попередження.

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

Повертає ім'я організації у разі успішного виконання або **`false`**, якщо адреса не може бути знайдена в базі даних.

### Приклади

**Приклад #1 Приклад використання**geoiporgбname()\*\*\*\*

Буде виведено назву організації, якій належить IP-адреса хоста example.com.

```php
<?php
$org = geoip_org_by_name('www.example.com');
if ($org) {
    echo 'Владелец данного адреса: ' . $org;
}
?>
```

Результат виконання цього прикладу:

```
Владелец данного адреса: ICANN c/o Internet Assigned Numbers Authority
```