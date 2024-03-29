---
navigation:
  - function.wincache-lock.md: « wincache\_lock
  - function.wincache-ocache-meminfo.md: wincache\_ocache\_meminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ocache\_fileinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ocache\_fileinfo

(PECL wincache >= 1.0.0)

wincache\_ocache\_fileinfo — Отримує інформацію про файли, закешовані в кеші опкодів

### Опис

```methodsynopsis
wincache_ocache_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст кешу опкодів та його використання.

**Увага**

Ця функція *ВИДАЛЕНО* у PHP 7.0.0.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кеша разом зі зведенням кеша опкодів.

### Значення, що повертаються

Масив метаданих про кеш опкодів або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime`\- загальний час на секундах, протягом якого кеш опкода був активний.
    
-   `total_file_count`\- загальна кількість файлів, які зараз перебувають у кеші опкодів.
    
-   `total_hit_count`\- кількість разів, коли скомпільований опкод використали з кеша.
    
-   `total_miss_count`\- кількість разів, коли скомпільований опкод не знайдено в кеші.
    
-   `is_local_cache`\- true, якщо метадані кешу призначені для екземпляра локального кешу, false, якщо метадані призначені для глобального кешу.
    
-   `file_entries`\- масив, що містить інформацію про всі файли, що закешуються:
    
    -   `file_name`\- Абсолютне ім'я файлу, що закешується.
    -   `add_time`\- час у секундах з моменту додавання файлу до кешу опкодів.
    -   `use_time`\- час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check`\- час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `hit_count`\- кількість разів, коли файл використали з кеша.
    -   `function_count`\- кількість функцій у зашифрованому файлі.
    -   `class_count`\- кількість класів у зашифрованому файлі.

### Приклади

**Приклад #1 Приклад використання** wincache\_ocache\_fileinfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_ocache_fileinfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
