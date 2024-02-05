---
navigation:
  - function.memory-reset-peak-usage.md: « memory\_reset\_peak\_usage
  - function.php-ini-scanned-files.md: php\_ini\_scanned\_files »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: php\_ini\_loaded\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_ini\_loaded\_file

(PHP 5 >= 5.2.4, PHP 7, PHP 8)

php\_ini\_loaded\_file — Отримати шлях до завантаженого файлу php.ini

### Опис

```methodsynopsis
php_ini_loaded_file(): string|false
```

Перевіряє, чи завантажено файл php.ini, і повертає його шлях.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Путь к загруженному файлу php.ini или\*\*`false`\*\*, якщо файл не завантажено.

### Приклади

**Пример #1 Пример использования**php\_ini\_loaded\_file()\*\*\*\*

```php
<?php
$inipath = php_ini_loaded_file();

if ($inipath) {
    echo 'Загруженный php.ini: ' . $inipath;
} else {
    echo 'Файл php.ini не загружен';
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Loaded php.ini: /usr/local/php/php.ini
```

### Дивіться також

-   [php\_ini\_scanned\_files()](function.php-ini-scanned-files.md) \- Повертає список .ini-файлів, знайдених у додатковій ini-директорії
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [Конфігураційний файл](configuration.file.md)
