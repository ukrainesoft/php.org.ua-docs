Отримує інформацію про використання пам'яті кешу користувача.

-   [« wincacheucacheinfo](function.wincache-ucache-info.html)
    
-   [wincacheucacheset »](function.wincache-ucache-set.html)
    
-   [PHP Manual](index.md)
    
-   [Функции WinCache](ref.wincache.md)
    
-   Отримує інформацію про використання пам'яті кешу користувача.
    

# wincacheucachememinfo

(PECL wincache >= 1.1.0)

wincacheucachememinfo — Отримує інформацію про використання пам'яті кешу користувача.

### Опис

```methodsynopsis
wincache_ucache_meminfo(): array|false
```

Отримує інформацію про використання пам'яті кешу користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання пам'яті користувача кешу або **`false`** у разі виникнення помилки

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total` - обсяг пам'яті в байтах, виділений для користувальницького кешу
-   `memory_free` - обсяг вільної пам'яті в байтах, доступної для користувальницького кешу
-   `num_used_blks` - кількість блоків пам'яті, що використовуються кешем користувача
-   `num_free_blks` - кількість вільних блоків пам'яті, доступних для користувальницького кешу
-   `memory_overhead` - обсяг пам'яті в байтах, що використовується для внутрішніх структур кешу користувача

### Приклади

**Приклад #1 Приклад використання **wincacheucachememinfo()****

```php
<pre>
<?php
print_r(wincache_ucache_meminfo());
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
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії