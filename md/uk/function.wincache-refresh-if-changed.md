Оновлює записи кешу для закешованих файлів

-   [« wincache\_ocache\_meminfo](function.wincache-ocache-meminfo.html)
    
-   [wincache\_rplist\_fileinfo »](function.wincache-rplist-fileinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Оновлює записи кешу для закешованих файлів
    

# wincacherefreshіфchanged

(PECL wincache >= 1.0.0)

wincacherefreshіфchanged — Оновлює записи кешу для файлів, що закешуються.

### Опис

```methodsynopsis
wincache_refresh_if_changed(array $files = NULL): bool
```

Оновлює записи кеша для файлів, імена яких були передані у вхідний аргумент. Якщо аргумент не вказано, всі записи в кеші оновлюються.

### Список параметрів

`files`

Масив імен файлів, які потрібно оновити. Можуть використовуватися абсолютні чи відносні шляхи до файлів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

WinCache виконує регулярні перевірки закешованих файлів, щоб гарантувати, що якщо якийсь файл було змінено, то відповідний запис у кеші буде оновлено. За промовчанням ця перевірка виконується кожні 30 секунд. Якщо, наприклад, PHP-скрипт оновлює інший PHP-скрипт, в якому зберігаються параметри конфігурації програми, то може статися так, що після збереження параметрів конфігурації у файл додаток, як і раніше, буде використовувати старі параметри протягом деякого часу, доки не буде оновлено кеш . У таких випадках може бути краще оновити кеш одразу після зміни файлу. У наведеному нижче прикладі показано, як це можна зробити.

**Приклад #1 Приклад використання **wincacherefreshіфchanged()****

```php
<?php
$filename = 'C:\inetpub\wwwroot\config.php';
$handle = fopen($filename, 'w+');
if ($handle === FALSE) die('Failed to open file '.$filename.' for writing');
fwrite($handle, '<?php $setting=something; ?>');
fclose($handle);
wincache_refresh_if_changed(array($filename));
?>
```

### Дивіться також

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача