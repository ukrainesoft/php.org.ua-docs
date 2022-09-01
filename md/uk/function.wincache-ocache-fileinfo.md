---
navigation:
  - function.wincache-lock.html: « wincachelock
  - function.wincache-ocache-meminfo.html: wincacheocachememinfo »
  - index.html: PHP Manual
  - ref.wincache.html: Функции WinCache
title: wincacheocachefileinfo
---
# wincacheocachefileinfo

(PECL wincache >= 1.0.0)

wincacheocachefileinfo — Отримує інформацію про файли, закешовані в кеші опкодів

### Опис

```methodsynopsis
wincache_ocache_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст кешу опкодів та його використання.

**Увага**

Ця функція *ВИДАЛЕНО* у PHP 7.0.0.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кешу разом із зведенням кешу опкодів.

### Значення, що повертаються

Масив метаданих про кеш опкодів або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime` - загальний час на секундах, протягом якого кеш опкода був активний.
    
-   `total_file_count` - загальна кількість файлів, які зараз перебувають у кеші опкодів.
    
-   `total_hit_count` - кількість разів, коли скомпільований опкод використали з кеша.
    
-   `total_miss_count` - кількість разів, коли скомпільований опкод не знайдено в кеші.
    
-   `is_local_cache` - true, якщо метадані кешу призначені для екземпляра локального кеша, false, якщо метадані призначені для глобального кешу.
    
-   `file_entries` - масив, що містить інформацію про всі зашифровані файли:
    
    -   `file_name` - Абсолютне ім'я файлу, що закешується.
    -   `add_time` - час у секундах з моменту додавання файлу до кешу опкодів.
    -   `use_time` - час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check` - час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `hit_count` - кількість разів, коли файл використали з кеша.
    -   `function_count` - кількість функцій у зашифрованому файлі.
    -   `class_count` - кількість класів у зашифрованому файлі.

### Приклади

**Приклад #1 Приклад використання **wincacheocachefileinfo()****

```php
<pre>
<?php
print_r(wincache_ocache_fileinfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [total_cache_uptime] => 17357
    [total_file_count] => 121
    [total_hit_count] => 36562
    [total_miss_count] => 201
    [file_entries] => Array
        (
            [1] => Array
                (
                    [file_name] => c:\inetpub\wwwroot\checkcache.php
                    [add_time] => 17356
                    [use_time] => 7
                    [last_check] => 10
                    [hit_count] => 454
                    [function_count] => 0
                    [class_count] => 1
                )
            [2] => Array (...iterates for each cached file)
        )
)
```

### Дивіться також

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії
