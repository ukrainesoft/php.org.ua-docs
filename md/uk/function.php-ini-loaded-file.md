Отримати шлях до завантаженого файлу php.ini

-   [« memory\_get\_usage](function.memory-get-usage.html)
    
-   [php\_ini\_scanned\_files »](function.php-ini-scanned-files.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Отримати шлях до завантаженого файлу php.ini
    

# phpiniloadedfile

(PHP 5> = 5.2.4, PHP 7, PHP 8)

phpiniloadedfile — Отримати шлях до завантаженого файлу php.ini

### Опис

```methodsynopsis
php_ini_loaded_file(): string|false
```

Перевіряє, чи завантажено файл php.ini, і повертає його шлях.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Шлях до завантаженого файлу php.ini або **`false`**, якщо файл не завантажено.

### Приклади

**Приклад #1 Приклад використання **phpiniloadedfile()****

```php
<?php
$inipath = php_ini_loaded_file();

if ($inipath) {
    echo 'Загруженный php.ini: ' . $inipath;
} else {
    echo 'Файл php.ini не загружен';
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Loaded php.ini: /usr/local/php/php.ini
```

### Дивіться також

-   [php\_ini\_scanned\_files()](function.php-ini-scanned-files.html) - Повертає список .ini-файлів, знайдених у додатковій ini-директорії
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [Конфигурационный файл](configuration.file.html)