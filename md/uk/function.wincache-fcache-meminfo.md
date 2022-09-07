---
navigation:
  - function.wincache-fcache-fileinfo.md: « wincachefcachefileinfo
  - function.wincache-lock.md: wincachelock »
  - index.md: PHP Manual
  - ref.wincache.md: Функции WinCache
title: wincachefcachememinfo
---
# wincachefcachememinfo

(PECL wincache >= 1.0.0)

wincachefcachememinfo — Отримує інформацію про використання пам'яті файлового кешу

### Опис

```methodsynopsis
wincache_fcache_meminfo(): array|false
```

Отримує інформацію щодо використання пам'яті файлового кеша.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання пам'яті файлового кешу або **`false`** у разі виникнення помилки

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total` - Об'єм пам'яті в байтах, виділений для файлового кешу
-   `memory_free` - Об'єм вільної пам'яті в байтах, доступної для файлового кешу.
-   `num_used_blks` - кількість блоків пам'яті, які використовуються файловим кешем
-   `num_free_blks` - кількість вільних блоків пам'яті, доступних для файлового кешу
-   `memory_overhead` - Об'єм пам'яті в байтах, що використовується для внутрішніх структур файлового кешу.

### Приклади

**Приклад #1 Приклад використання **wincachefcachememinfo()****

```php
<pre>
<?php
print_r(wincache_fcache_meminfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [memory_total] => 134217728
    [memory_free] => 131339120
    [num_used_blks] => 361
    [num_free_blks] => 3
    [memory_overhead] => 5856
)
```

### Дивіться також

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.md) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.md) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.md) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.md) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.md) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.md) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.md) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.md) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.md) - Отримує інформацію про використання кеш-пам'яті сесії
