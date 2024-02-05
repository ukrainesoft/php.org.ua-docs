---
navigation:
  - function.wincache-scache-info.md: « wincache\_scache\_info
  - function.wincache-ucache-add.md: wincache\_ucache\_add »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_scache\_meminfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_scache\_meminfo

(PECL wincache >= 1.1.0)

wincache\_scache\_meminfo — Отримує інформацію про використання кеш-пам'яті сесії

### Опис

```methodsynopsis
wincache_scache_meminfo(): array|false
```

Отримує інформацію щодо використання пам'яті кешем сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання кеш-пам'яті сесії або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total`\- Об'єм пам'яті в байтах, виділений для кеш-пам'яті сесії.
-   `memory_free`\- Об'єм вільної пам'яті в байтах, доступної для кеш-пам'яті сесії.
-   `num_used_blks`\- кількість блоків пам'яті, які використовуються кешем сесії.
-   `num_free_blks`\- Кількість вільних блоків пам'яті, доступних для кешу сесії.
-   `memory_overhead`\- Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешу сесії.

### Приклади

**Приклад #1 Приклад використання** wincache\_scache\_meminfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_scache_meminfo());
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
