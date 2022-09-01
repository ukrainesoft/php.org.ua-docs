---
navigation:
  - function.wincache-ocache-meminfo.html: « wincacheocachememinfo
  - function.wincache-rplist-fileinfo.html: wincacherplistfileinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacherefreshіфchanged
---
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

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.md) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.md) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.md) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.md) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.md) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
