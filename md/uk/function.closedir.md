Закриває дескриптор каталогу

-   [« chroot](function.chroot.html)
    
-   [dir »](function.dir.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з каталогами](ref.dir.html)
    
-   Закриває дескриптор каталогу
    

# closedir

(PHP 4, PHP 5, PHP 7, PHP 8)

closedir — Закриває дескриптор каталогу

### Опис

```methodsynopsis
closedir(?resource $dir_handle = null): void
```

Закриває потік, пов'язаний з каталогом і переданий як параметр `dir_handle`. Перед використанням цієї функції потік повинен бути відкритий за допомогою функції [opendir()](function.opendir.html)

### Список параметрів

`dir_handle`

Дескриптор каталогу (resource), раніше відкритий за допомогою [opendir()](function.opendir.html). Якщо дескриптор каталогу не вказано, використовується останній дескриптор, відкритий функцією [opendir()](function.opendir.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **closedir()****

```php
<?php
$dir = "/etc/php5/";

// Открываем известную директорию, читаем её в переменную и закрываем
if (is_dir($dir)) {
    if ($dh = opendir($dir)) {
        $directory = readdir($dh);
        closedir($dh);
    }
}
?>
```