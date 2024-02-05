---
navigation:
  - function.php-ini-loaded-file.md: « php\_ini\_loaded\_file
  - function.php-sapi-name.md: php\_sapi\_name »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: php\_ini\_scanned\_files
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_ini\_scanned\_files

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

php\_ini\_scanned\_files — Повертає список .ini-файлів, знайдених у додатковій ini-директорії

### Опис

```methodsynopsis
php_ini_scanned_files(): string|false
```

**php\_ini\_scanned\_files()** повертає список розділених комами конфігураційних файлів, проаналізованих після php.ini. Директорії, в яких проводиться пошук, задаються при компіляції та, опціонально, змінному оточенні під час виконання. Більше інформації можна знайти у [інструкції з встановлення](configuration.file.md#configuration.file.scan)

Імена файлів, що повертаються, включають повний шлях.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

При успіху повертає рядок із розділеними комами .ini-файлів. За кожною комою слідує новий рядок. Якщо директива **\--with-config-file-scan-dir** не задана та змінна оточення PHP\_INI\_SCAN\_DIR теж не задана, функція поверне **`false`**. Якщо директива поставлена ​​і порожня, буде повернено порожній рядок. Якщо файл не вдається розпізнати, він все ж таки буде включений до списку, але при цьому PHP повідомить про помилку. Ця помилка буде виникати як під час компіляції, так і під час роботи **php\_ini\_scanned\_files()**

### Приклади

**Приклад #1 Простий приклад виведення списку ini-файлів**

```php
<?php
if ($filelist = php_ini_scanned_files()) {
    if (strlen($filelist) > 0) {
        $files = explode(',', $filelist);

        foreach ($files as $file) {
            echo "<li>" . trim($file) . "</li>\n";
        }
    }
}
?>
```

### Дивіться також

-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [php\_ini\_loaded\_file()](function.php-ini-loaded-file.md) \- Отримати шлях до завантаженого файлу php.ini
