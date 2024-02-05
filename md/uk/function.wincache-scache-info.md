---
navigation:
  - function.wincache-rplist-meminfo.md: « wincache\_rplist\_meminfo
  - function.wincache-scache-meminfo.md: wincache\_scache\_meminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_scache\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_scache\_info

(PECL wincache >= 1.1.0)

wincache\_scache\_info — Отримує інформацію про файли, закешовані в кеші сесії

### Опис

```methodsynopsis
wincache_scache_info(bool $summaryonly = false): array|false
```

Отримує інформацію про вміст кешу сесії та його використання.

### Список параметрів

`summaryonly`

Визначає, чи масив, що повертається, міститиме інформацію про окремі записи кешу разом із зведенням кешу сесії.

### Значення, що повертаються

Масив метаданих про кеш сесії або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime`\- загальний час на секундах, протягом якого кеш сесії був активний.
    
-   `total_item_count`\- загальна кількість елементів, які зараз перебувають у кеші сесії.
    
-   `is_local_cache`\- true, якщо метадані кешу призначені для екземпляра локального кешу, false, якщо метадані призначені для глобального кешу.
    
-   `total_hit_count`\- кількість разів, коли дані було оброблено з кешу.
    
-   `total_miss_count`\- кількість разів, коли дані не знайшли в кеші.
    
-   `scache_entries`\- масив, що містить інформацію про всі закешовані елементи:
    
    -   `key_name`\- Ім'я ключа, який використовується для зберігання даних.
    -   `value_type`\- Тип значення, що зберігається ключем.
    -   `use_time`\- час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check`\- час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `ttl_seconds`\- час, що залишився для даних, щоб залишатися в кеші, означає 0 нескінченність.
    -   `age_seconds`\- час, що минув з моменту додавання даних у кеш.
    -   `hitcount`\- кількість разів, коли дані було отримано з кешу.

### Приклади

**Пример #1 Пример использования**wincache\_scache\_info()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_scache_info());
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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
