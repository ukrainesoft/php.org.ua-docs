---
navigation:
  - ref.wincache.md: « Функції WinCache
  - function.wincache-fcache-meminfo.md: wincache\_fcache\_meminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_fcache\_fileinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_fcache\_fileinfo

(PECL wincache >= 1.0.0)

wincache\_fcache\_fileinfo — Отримує інформацію про файли, закешовані у файловому кеші

### Опис

```methodsynopsis
wincache_fcache_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст файлового кеша та його використання.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кеша разом зі зведенням файлового кеша.

### Значення, що повертаються

Масив метаданих про файловий кеш або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime`\- загальний час у секундах, протягом якого файловий кеш був активним
    
-   `total_file_count`\- загальна кількість файлів, які зараз знаходяться у файловому кеші
    
-   `total_hit_count`\- кількість разів, коли файли обслуговувалися із файлового кешу
    
-   `total_miss_count`\- кількість разів, коли файли не знайшли в файловому кеші
    
-   `file_entries`\- масив, що містить інформацію про всі файли, що закешуються:
    
    -   `file_name`\- абсолютне ім'я закешованого файлу
    -   `add_time`\- час у секундах з моменту додавання файлу до кешу
    -   `use_time`\- час у секундах з моменту звернення до файлу у кеші
    -   `last_check`\- час у секундах з моменту перевірки файлу на наявність модифікацій
    -   `hit_count`\- кількість разів, коли файл був оброблений із кешу
    -   `file_size`\- Розмір файлу, що кешується в байтах

### Приклади

**Пример #1 Пример использования**wincache\_fcache\_fileinfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_fcache_fileinfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
