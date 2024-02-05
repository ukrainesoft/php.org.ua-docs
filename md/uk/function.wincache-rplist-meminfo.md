---
navigation:
  - function.wincache-rplist-fileinfo.md: « wincache\_rplist\_fileinfo
  - function.wincache-scache-info.md: wincache\_scache\_info »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_rplist\_meminfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_rplist\_meminfo

(PECL wincache >= 1.0.0)

wincache\_rplist\_meminfo — Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності

### Опис

```methodsynopsis
wincache_rplist_meminfo(): array|false
```

Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих, що описує використання пам'яті за допомогою кеша шляху до файлу роздільної здатності або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total`\- Об'єм пам'яті в байтах, виділений для кеша шляху до файлу дозволу.
-   `memory_free`\- Об'єм вільної пам'яті в байтах, доступної для кеша шляху до файлу дозволу.
-   `num_used_blks`\- кількість блоків пам'яті, які використовуються кешем шляху до файлу роздільної здатності.
-   `num_free_blks`\- кількість вільних блоків пам'яті, доступних для кеша шляху файлу дозволу.
-   `memory_overhead`\- Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешування шляху до файлу дозволу.

### Приклади

**Пример #1 Пример использования**wincache\_rplist\_meminfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_rplist_meminfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
