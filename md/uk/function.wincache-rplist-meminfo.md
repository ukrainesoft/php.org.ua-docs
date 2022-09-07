---
navigation:
  - function.wincache-rplist-fileinfo.md: « wincacherplistfileinfo
  - function.wincache-scache-info.md: wincachescacheinfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincacherplistmeminfo
---
# wincacherplistmeminfo

(PECL wincache >= 1.0.0)

wincacherplistmeminfo — Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності

### Опис

```methodsynopsis
wincache_rplist_meminfo(): array|false
```

Отримує інформацію про використання пам'яті за допомогою кеша шляху до роздільної здатності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих, що описує використання пам'яті за допомогою кеша шляху до файлу роздільної здатності або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total` - Об'єм пам'яті в байтах, виділений для кеша шляху до файлу дозволу.
-   `memory_free` - Об'єм вільної пам'яті в байтах, доступної для кеша шляху до файлу дозволу.
-   `num_used_blks` - кількість блоків пам'яті, які використовуються кешем шляху до файлу роздільної здатності.
-   `num_free_blks` - кількість вільних блоків пам'яті, доступних для кеша шляху файлу дозволу.
-   `memory_overhead` - Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешування шляху до файлу дозволу.

### Приклади

**Приклад #1 Приклад використання **wincacherplistmeminfo()****

```php
<pre>
<?php
print_r(wincache_rplist_meminfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [memory_total] => 9437184
    [memory_free] => 9416744
    [num_used_blks] => 23
    [num_free_blks] => 1
    [memory_overhead] => 416
)
```

### Дивіться також

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.md) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.md) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.md) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.md) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.md) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.md) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті сесії
