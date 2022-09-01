---
navigation:
  - function.gethostbynamel.md: « gethostbynamel
  - function.getmxrr.md: getmxrr »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostname
---
# gethostname

(PHP 5> = 5.3.0, PHP 7, PHP 8)

gethostname — Отримує ім'я хоста

### Опис

```methodsynopsis
gethostname(): string|false
```

Функція **gethostname()** отримує стандартну назву хоста для локального комп'ютера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з ім'ям хоста або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gethostname()****

```php
<?php
echo gethostname(); // может вывести например: sandie
?>
```

### Дивіться також

-   [gethostbyname()](function.gethostbyname.md) - Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.md) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [phpuname()](function.php-uname.md) - Повертає інформацію про операційну систему, на якій запущено PHP
