---
navigation:
  - function.memory-get-usage.html: « memorygetusage
  - function.php-ini-scanned-files.html: phpiniscannedfiles »
  - index.html: PHP Manual
  - ref.info.html: Опції PHP/інформаційні функції
title: phpiniloadedfile
---
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

-   [phpiniscannedfiles()](function.php-ini-scanned-files.html) - Повертає список .ini-файлів, знайдених у додатковій ini-директорії
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [Конфігураційний файл](configuration.file.html)
