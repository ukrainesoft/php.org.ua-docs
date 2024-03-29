---
navigation:
  - function.gethostbyname.md: « gethostbyname
  - function.gethostname.md: gethostname »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostbynamel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gethostbynamel

(PHP 4, PHP 5, PHP 7, PHP 8)

gethostbynamel — Отримує список IPv4-адрес, що відповідають переданому доменному імені хоста

### Опис

```methodsynopsis
gethostbynamel(string $hostname): array|false
```

Повертає список IPv4-адрес, у яких дозволяється доменне ім'я хоста `hostname`

### Список параметрів

`hostname`

Ім'я хоста.

### Значення, що повертаються

Повертає масив адрес IPv4 або **`false`**, якщо `hostname` не може бути дозволено.

### Приклади

**Приклад #1 Приклад використання функції** gethostbynamel()\*\*\*\*

```php
<?php
$hosts = gethostbynamel('www.example.com');
print_r($hosts);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => 192.0.34.166
)
```

### Дивіться також

-   [gethostbyname()](function.gethostbyname.md) \- Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.md) \- Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [checkdnsrr()](function.checkdnsrr.md) \- Перевіряє записи DNS, що відповідають переданому імені вузла Інтернету або IP-адресі
-   [getmxrr()](function.getmxrr.md) \- Отримує записи MX, що відповідають переданому доменному імені хоста
-   the`named(8)`manual page
