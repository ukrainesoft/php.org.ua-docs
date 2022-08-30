Повертає змінну оточення підпроцесу сервера Apache

-   [« apachegetversion](function.apache-get-version.html)
    
-   [apachelookupuri »](function.apache-lookup-uri.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Apache](ref.apache.html)
    
-   Повертає змінну оточення підпроцесу сервера Apache
    

# apachegetenv

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

apachegetenv — Повертає змінну оточення підпроцесу сервера Apache

### Опис

```methodsynopsis
apache_getenv(string $variable, bool $walk_to_top = false): string|false
```

Повертає змінну оточення сервера Apache, вказану параметром `variable`

### Список параметрів

`variable`

Змінне оточення сервера Apache

`walk_to_top`

Отримати змінну верхнього рівня, доступну для всіх рівнів Apache сервера чи ні.

### Значення, що повертаються

Значення змінної оточення сервера Apache у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apachegetenv()****

Нижче наведений приклад показує, як можна отримати значення змінної оточення сервера Apache SERVERADDR.

```php
<?php
$ret = apache_getenv("SERVER_ADDR");
echo $ret;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
42.24.42.240
```

### Дивіться також

-   [apachesetenv()](function.apache-setenv.html) - Встановлює змінну subprocessenv Apache
-   [getenv()](function.getenv.html) - набуття значення змінної оточення
-   "[Суперглобальные переменные](language.variables.superglobals.html)"