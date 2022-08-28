Повертає список .ini-файлів, знайдених у додатковій ini-директорії

-   [« php\_ini\_loaded\_file](function.php-ini-loaded-file.html)
    
-   [php\_sapi\_name »](function.php-sapi-name.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Повертає список .ini-файлів, знайдених у додатковій ini-директорії
    

# phpiniscannedfiles

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

phpiniscannedfiles — Повертає список .ini-файлів, знайдених у додатковій ini-директорії

### Опис

```methodsynopsis
php_ini_scanned_files(): string|false
```

**phpiniscannedfiles()** повертає список розділених комами конфігураційних файлів, проаналізованих після php.ini. Директорії, в яких проводиться пошук, задаються при компіляції та, опціонально, змінному оточенні під час виконання. Більше інформації можна знайти у [инструкции по установке](configuration.file.html#configuration.file.scan)

Імена файлів, що повертаються, включають повний шлях.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

При успіху повертає рядок із розділеними комами .ini-файлів. За кожною комою слідує новий рядок. Якщо директива **\-with-config-file-scan-dir** не задана та змінна оточення PHPINISCANDIR теж не задана, функція поверне **`false`**. Якщо директива поставлена ​​і порожня, буде повернено порожній рядок. Якщо файл не вдається розпізнати, він все ж таки буде включений до списку, але при цьому PHP повідомить про помилку. Ця помилка буде виникати як під час компіляції, так і під час роботи **phpiniscannedfiles()**

### Приклади

**Приклад #1 Простий приклад виведення списку ini-файлів**

```php
<?php
if ($filelist = php_ini_scanned_files()) {
    if (strlen($filelist) > 0) {
        $files = explode(',', $filelist);

        foreach ($files as $file) {
            echo "<li>" . trim($file) . "</li>\n";
        }
    }
}
?>
```

### Дивіться також

-   [ini\_set()](function.ini-set.html) - Встановлює налаштування конфігурації
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP
-   [php\_ini\_loaded\_file()](function.php-ini-loaded-file.html) - Отримати шлях до завантаженого файлу php.ini