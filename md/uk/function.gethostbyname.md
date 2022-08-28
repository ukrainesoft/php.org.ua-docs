Отримує IPv4-адресу, що відповідає переданому імені хоста

-   [« gethostbyaddr](function.gethostbyaddr.html)
    
-   [gethostbynamel »](function.gethostbynamel.html)
    
-   [PHP Manual](index.html)
    
-   [Сетевые функции](ref.network.html)
    
-   Отримує IPv4-адресу, що відповідає переданому імені хоста
    

# gethostbyname

(PHP 4, PHP 5, PHP 7, PHP 8)

gethostbyname — Отримує IPv4-адресу, що відповідає переданому імені хоста

### Опис

```methodsynopsis
gethostbyname(string $hostname): string
```

Повертає IPv4-адресу на ім'я хоста `hostname`

### Список параметрів

`hostname`

Ім'я вузла.

### Значення, що повертаються

Повертає адресу IPv4 або рядок, що містить незмінений `hostname` у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад використання **gethostbyname()****

```php
<?php
$ip = gethostbyname('www.example.com');

echo $ip;
?>
```

### Дивіться також

-   [gethostbyaddr()](function.gethostbyaddr.html) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [gethostbynamel()](function.gethostbynamel.html) - Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   [inet\_pton()](function.inet-pton.html) - Конвертує IP-адресу, що читається, в її упаковане подання inaddr
-   [inet\_ntop()](function.inet-ntop.html) - Конвертує упаковану інтернет-адресу в формат, що читається