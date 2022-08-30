Отримує ім'я хоста

-   [« gethostbynamel](function.gethostbynamel.html)
    
-   [getmxrr »](function.getmxrr.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Отримує ім'я хоста
    

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

-   [gethostbyname()](function.gethostbyname.html) - Отримує IPv4-адресу, що відповідає переданому імені хоста
-   [gethostbyaddr()](function.gethostbyaddr.html) - Отримує доменне ім'я хоста, що відповідає переданій IP-адресі
-   [phpuname()](function.php-uname.html) - Повертає інформацію про операційну систему, на якій запущено PHP