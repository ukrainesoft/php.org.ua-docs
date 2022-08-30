Отримує інформацію про використання кеш-пам'яті опкодів

-   [« wincacheocachefileinfo](function.wincache-ocache-fileinfo.html)
    
-   [wincacherefreshіфchanged »](function.wincache-refresh-if-changed.html)
    
-   [PHP Manual](index.md)
    
-   [Функции WinCache](ref.wincache.md)
    
-   Отримує інформацію про використання кеш-пам'яті опкодів
    

# wincacheocachememinfo

(PECL wincache >= 1.0.0)

wincacheocachememinfo — Отримує інформацію про використання кеш-пам'яті опкодів

### Опис

```methodsynopsis
wincache_ocache_meminfo(): array|false
```

Отримує інформацію про використання кеш-пам'яті опкодів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання кеш-пам'яті опкодів або **`false`** у разі виникнення помилки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total` - Об'єм пам'яті в байтах, виділений для кеша опкодів.
-   `memory_free` - Об'єм вільної пам'яті в байтах, доступної для кеша опкодів.
-   `num_used_blks` - кількість блоків пам'яті, які використовуються кешем опкодів.
-   `num_free_blks` - Кількість вільних блоків пам'яті, доступних для кешу опкодів.
-   `memory_overhead` - Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешу опкодів.

**Увага**

Ця функція *ВИДАЛЕНО* у PHP 7.0.0.

### Приклади

**Приклад #1 Приклад використання **wincacheocachememinfo()****

```php
<pre>
<?php
print_r(wincache_ocache_meminfo());
?>
</pre>
```

Результат виконання цього прикладу:

```
Array
(
    [memory_total] => 134217728
    [memory_free] => 112106972
    [num_used_blks] => 15469
    [num_free_blks] => 4
    [memory_overhead] => 247600
)
```

### Дивіться також

-   [wincachefcachefileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincacheucacheinfo()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincachescacheinfo()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії