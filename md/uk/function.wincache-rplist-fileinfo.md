---
navigation:
  - function.wincache-refresh-if-changed.md: « wincacherefreshіфchanged
  - function.wincache-rplist-meminfo.md: wincacherplistmeminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacherplistfileinfo
---
# wincacherplistfileinfo

(PECL wincache >= 1.0.0)

wincacherplistfileinfo — Отримує інформацію про дозвіл кешу шляху до файлу дозволу

### Опис

```methodsynopsis
wincache_rplist_fileinfo(bool $summaryonly = false): array|false
```

Отримує інформацію про закешовані зіставлення між відносними шляхами до файлів і абсолютними відповідними шляхами до файлів.

### Список параметрів

`summaryonly`

### Значення, що повертаються

Масив метаданих про кеш шляху до файлу дозволу або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `total_file_count` - загальна кількість зіставлень шляху до файлу, які у кеші.
    
-   `rplist_entries` - масив, що містить інформацію про всі шляхи зашифрованих файлів:
    
    -   `resolve_path` - шлях до файлу.
    -   `subkey_data` - Відповідний абсолютний шлях до файлу.

### Приклади

**Приклад #1 Приклад використання **wincacherplistfileinfo()****

```php
<pre>
<?php
print_r(wincache_rplist_fileinfo());
?>
</pre>
```

Результат виконання цього прикладу:

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

-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.md) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.md) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.md) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.md) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.md) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.md) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті сесії
