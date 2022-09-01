---
navigation:
  - function.gethostbyaddr.md: « gethostbyaddr
  - function.gethostbynamel.md: gethostbynamel »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostbyname
---
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

-   [gethostbyaddr()](function.gethostbyaddr.md) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [gethostbynamel()](function.gethostbynamel.md) - Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   [inetpton()](function.inet-pton.md) - Конвертує IP-адресу, що читається, в її упаковане подання inaddr
-   [inetntop()](function.inet-ntop.md) - Конвертує упаковану інтернет-адресу в формат, що читається
