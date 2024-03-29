---
navigation:
  - function.gethostbynamel.md: « gethostbynamel
  - function.getmxrr.md: getmxrr »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: gethostname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gethostname

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gethostname — Отримує ім'я хоста

### Опис

```methodsynopsis
gethostname(): string|false
```

Функция\*\*gethostname()\*\*получает стандартное имя хоста для локального компьютера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок з ім'ям хоста або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gethostname()\*\*\*\*

```php
<?php
echo gethostname(); // может вывести наПриклад: sandie
?>
```

### Дивіться також

-   [gethostbyname()](function.gethostbyname.md) \- Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.md) \- Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [php\_uname()](function.php-uname.md) \- Повертає інформацію про операційну систему, на якій запущено PHP
