Отримує інформацію про використання кеш-пам'яті сесії

-   [« wincachescacheinfo](function.wincache-scache-info.html)
    
-   [wincacheucacheadd »](function.wincache-ucache-add.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Отримує інформацію про використання кеш-пам'яті сесії
    

# wincachescachememinfo

(PECL wincache >= 1.1.0)

wincachescachememinfo — Отримує інформацію про використання кеш-пам'яті сесії

### Опис

```methodsynopsis
wincache_scache_meminfo(): array|false
```

Отримує інформацію щодо використання пам'яті кешем сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання кеш-пам'яті сесії або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total` - Об'єм пам'яті в байтах, виділений для кеш-пам'яті сесії.
-   `memory_free` - Об'єм вільної пам'яті в байтах, доступної для кеш-пам'яті сесії.
-   `num_used_blks` - кількість блоків пам'яті, які використовуються кешем сесії.
-   `num_free_blks` - Кількість вільних блоків пам'яті, доступних для кешу сесії.
-   `memory_overhead` - Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешу сесії.

### Приклади

**Приклад #1 Приклад використання **wincachescachememinfo()****

```php
<pre>
<?php
print_r(wincache_scache_meminfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [memory_total] => 5242880
    [memory_free] => 5215056
    [num_used_blks] => 6
    [num_free_blks] => 3
    [memory_overhead] => 176
)
```

### Дивіться також

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії