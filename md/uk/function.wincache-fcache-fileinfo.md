Отримує інформацію про файли, закешовані у файловому кеші

-   [« Функции WinCache](ref.wincache.html)
    
-   [wincachefcachememinfo »](function.wincache-fcache-meminfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Отримує інформацію про файли, закешовані у файловому кеші
    

# wincachefcachefileinfo

(PECL wincache >= 1.0.0)

wincachefcachefileinfo — Отримує інформацію про файли, закешовані у файловому кеші

### Опис

```methodsynopsis
wincache_fcache_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст файлового кеша та його використання.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кеша разом зі зведенням файлового кеша.

### Значення, що повертаються

Масив метаданих про файловий кеш або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime` - загальний час у секундах, протягом якого файловий кеш був активним
    
-   `total_file_count` - загальна кількість файлів, які зараз знаходяться у файловому кеші
    
-   `total_hit_count` - кількість разів, коли файли обслуговувалися із файлового кешу
    
-   `total_miss_count` - кількість разів, коли файли не знайшли в файловому кеші
    
-   `file_entries` - масив, що містить інформацію про всі зашифровані файли:
    
    -   `file_name` - абсолютне ім'я закешованого файлу
    -   `add_time` - час у секундах з моменту додавання файлу до кешу
    -   `use_time` - час у секундах з моменту звернення до файлу у кеші
    -   `last_check` - час у секундах з моменту перевірки файлу на наявність модифікацій
    -   `hit_count` - кількість разів, коли файл був оброблений із кешу
    -   `file_size` - Розмір файлу, що кешується в байтах

### Приклади

**Приклад #1 Приклад використання **wincachefcachefileinfo()****

```php
<pre>
<?php
print_r(wincache_fcache_fileinfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(   [total_cache_uptime] => 3234
    [total_file_count] => 5
    [total_hit_count] => 0
    [total_miss_count] => 1
    [file_entries] => Array
        (
            [1] => Array
                (
                    [file_name] => c:\inetpub\wwwroot\checkcache.php
                    [add_time] => 1
                    [use_time] => 0
                    [last_check] => 1
                    [hit_count] => 1
                    [file_size] => 2435
                )
            [2] => Array (...iterates for each cached file)
        )
)
```

### Дивіться також

-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії