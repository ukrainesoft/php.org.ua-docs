---
navigation:
  - function.wincache-refresh-if-changed.md: « wincache\_refresh\_if\_changed
  - function.wincache-rplist-meminfo.md: wincache\_rplist\_meminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_rplist\_fileinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_rplist\_fileinfo

(PECL wincache >= 1.0.0)

wincache\_rplist\_fileinfo — Отримує інформацію про дозвіл кешу шляху до файлу дозволу

### Опис

```methodsynopsis
wincache_rplist_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про закешовані зіставлення між відносними шляхами до файлів і абсолютними відповідними шляхами до файлів.

### Список параметрів

`summaryonly`

### Значення, що повертаються

Масив метаданих про кеш шляху до файлу дозволу або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_file_count`\- загальна кількість зіставлень шляху до файлу, які у кеші.
    
-   `rplist_entries`\- масив, що містить інформацію про всі шляхи закешованих файлів:
    
    -   `resolve_path`\- шлях до файлу.
    -   `subkey_data`\- Відповідний абсолютний шлях до файлу.

### Приклади

**Приклад #1 Приклад використання** wincache\_rplist\_fileinfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_rplist_fileinfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

```
Array
(
    [total_file_count] => 5
    [rplist_entries] => Array
        (
            [1] => Array
                (
                    [resolve_path] => checkcache.php
                    [subkey_data] => c:\inetpub\wwwroot|c:\inetpub\wwwroot\checkcache.php
                )

            [2] => Array (...iterates for each cached file)
        )
)
```

### Дивіться також

-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
