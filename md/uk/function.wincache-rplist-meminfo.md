Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності

-   [« wincache\_rplist\_fileinfo](function.wincache-rplist-fileinfo.html)
    
-   [wincache\_scache\_info »](function.wincache-scache-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
    

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії