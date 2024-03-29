---
navigation:
  - function.fsockopen.md: « fsockopen
  - function.gethostbyname.md: gethostbyname »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostbyaddr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gethostbyaddr

(PHP 4, PHP 5, PHP 7, PHP 8)

gethostbyaddr — Отримує доменне ім'я хоста, що відповідає переданій IP-адресі

### Опис

```methodsynopsis
gethostbyaddr(string $ip): string|false
```

Возвращает доменное имя хоста по адресу`ip`

### Список параметрів

`ip`

IP-адреса хоста

### Значення, що повертаються

Повертає ім'я хоста у разі успішного виконання, вихідний `ip`в случае возникновения ошибки, или\*\*`false`\*\* у разі помилкового введення.

### Приклади

**Приклад #1 Простий приклад використання **gethostbyaddr()****

```php
<?php
$hostname = gethostbyaddr($_SERVER['REMOTE_ADDR']);

echo $hostname;
?>
```

### Дивіться також

-   [gethostbyname()](function.gethostbyname.md) \- Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbynamel()](function.gethostbynamel.md) \- Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
