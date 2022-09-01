---
navigation:
  - function.wincache-rplist-meminfo.html: « wincacherplistmeminfo
  - function.wincache-scache-meminfo.html: wincachescachememinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincachescacheinfo
---
# wincachescacheinfo

(PECL wincache >= 1.1.0)

wincachescacheinfo — Отримує інформацію про файли, закешовані в кеші сесії

### Опис

```methodsynopsis
wincache_scache_info(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст кешу сесії та його використання.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кешу разом із зведенням кешу сесії.

### Значення, що повертаються

Масив метаданих про кеш сесії або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime` - загальний час на секундах, протягом якого кеш сесії був активний.
    
-   `total_item_count` - загальна кількість елементів, які зараз перебувають у кеші сесії.
    
-   `is_local_cache` - true, якщо метадані кешу призначені для екземпляра локального кеша, false, якщо метадані призначені для глобального кешу.
    
-   `total_hit_count` - кількість разів, коли дані було оброблено з кешу.
    
-   `total_miss_count` - кількість разів, коли дані не знайшли в кеші.
    
-   `scache_entries` - масив, що містить інформацію про всі закешовані елементи:
    
    -   `key_name` - Ім'я ключа, який використовується для зберігання даних.
    -   `value_type` - Тип значення, що зберігається ключем.
    -   `use_time` - час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check` - час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `ttl_seconds` - час, що залишився для даних, щоб залишатися в кеші, означає 0 нескінченність.
    -   `age_seconds` - час, що минув з моменту додавання даних у кеш.
    -   `hitcount` - кількість разів, коли дані було отримано з кешу.

### Приклади

**Приклад #1 Приклад використання **wincachescacheinfo()****

```php
<pre>
<?php
print_r(wincache_scache_info());
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
    [scache_entries] => Array
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
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії
