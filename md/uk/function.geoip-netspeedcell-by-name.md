Отримати швидкість з'єднання з мережею Інтернет

-   [« geoipispбname](function.geoip-isp-by-name.html)
    
-   [geoiporgбname »](function.geoip-org-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GeoIP](ref.geoip.html)
    
-   Отримати швидкість з'єднання з мережею Інтернет
    

# geoipnetspeedcellбname

(PECL geoip >= 1.1.0)

geoipnetspeedcellбname — Отримати швидкість підключення до мережі Інтернет

### Опис

```methodsynopsis
geoip_netspeedcell_by_name(string $hostname): string
```

Функція **geoipnetspeedcellбname()** повертає тип підключення до мережі Інтернет та його швидкість щодо заданого імені хоста або IP-адреси.

Ця функція доступна лише тоді, коли використовується бібліотека GeoIP версії 1.4.8 та вище.

Зараз ця функція доступна лише користувачам, які купили комерційну версію GeoIP Domain Edition. Якщо коректна база даних не буде знайдена, буде виведено попередження.

Повертається рядок. Стандартні значення:

-   Cable/DSL
-   Dialup
-   Cellular
-   Corporate

### Список параметрів

`hostname`

Ім'я хоста або IP-адреса.

### Значення, що повертаються

У разі успішного виконання повертає швидкість з'єднання. Якщо адреса не знайдена у базі даних, то повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **geoipnetspeedcellбname()****

Отримання швидкості з'єднання з example.com.

```php
<?php
$netspeed = geoip_netspeedcell_by_name('www.example.com');

if ($netspeed) {
    echo 'Тип соединения: '. $netspeed;
}
?>
```

Результат виконання цього прикладу:

```
Тип соединения: Corporate
```