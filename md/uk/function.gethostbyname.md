---
navigation:
  - function.gethostbyaddr.md: « gethostbyaddr
  - function.gethostbynamel.md: gethostbynamel »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostbyname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gethostbyname

(PHP 4, PHP 5, PHP 7, PHP 8)

gethostbyname — Отримує IPv4-адресу, що відповідає переданому імені хоста

### Опис

```methodsynopsis
gethostbyname(string $hostname): string
```

Возвращает IPv4-адрес по имени хоста`hostname`

### Список параметрів

`hostname`

Ім'я вузла.

### Значення, що повертаються

Повертає адресу IPv4 або рядок, що містить незмінений `hostname`в случае возникновения ошибки.

### Приклади

**Приклад #1 Простий приклад використання **gethostbyname()****

```php
<?php
$ip = gethostbyname('www.example.com');

echo $ip;
?>
```

### Дивіться також

-   [gethostbyaddr()](function.gethostbyaddr.md) \- Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [gethostbynamel()](function.gethostbynamel.md) \- Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста
-   [inet\_pton()](function.inet-pton.md) \- Конвертує IP-адресу, що читається, в її упаковане подання in\_addr
-   [inet\_ntop()](function.inet-ntop.md) \- Конвертує упаковану інтернет-адресу в формат, що читається
