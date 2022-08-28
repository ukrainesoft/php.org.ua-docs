Отримує інформацію про використання пам'яті файлового кешу

-   [« wincache\_fcache\_fileinfo](function.wincache-fcache-fileinfo.html)
    
-   [wincache\_lock »](function.wincache-lock.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Отримує інформацію про використання пам'яті файлового кешу
    

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.html) - Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.html) - Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії