---
navigation:
  - function.wincache-ucache-info.md: « wincache\_ucache\_info
  - function.wincache-ucache-set.md: wincache\_ucache\_set »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_meminfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_meminfo

(PECL wincache >= 1.1.0)

wincache\_ucache\_meminfo — Отримує інформацію про використання пам'яті кешу користувача.

### Опис

```methodsynopsis
wincache_ucache_meminfo(): array|false
```

Отримує інформацію про використання пам'яті кешу користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання пам'яті користувача кешу або \*\*`false`\*\*в случае возникновения ошибки

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total`\- обсяг пам'яті в байтах, виділений для користувальницького кешу
-   `memory_free`\- обсяг вільної пам'яті в байтах, доступної для користувальницького кешу
-   `num_used_blks`\- кількість блоків пам'яті, що використовуються кешем користувача
-   `num_free_blks`\- кількість вільних блоків пам'яті, доступних для користувальницького кешу
-   `memory_overhead`\- обсяг пам'яті в байтах, що використовується для внутрішніх структур кешу користувача

### Приклади

**Приклад #1 Приклад використання** wincache\_ucache\_meminfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_ucache_meminfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
