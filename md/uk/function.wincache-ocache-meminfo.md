---
navigation:
  - function.wincache-ocache-fileinfo.md: « wincache\_ocache\_fileinfo
  - function.wincache-refresh-if-changed.md: wincache\_refresh\_if\_changed »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ocache\_meminfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ocache\_meminfo

(PECL wincache >= 1.0.0)

wincache\_ocache\_meminfo — Отримує інформацію про використання кеш-пам'яті опкодів

### Опис

```methodsynopsis
wincache_ocache_meminfo(): array|false
```

Отримує інформацію про використання кеш-пам'яті опкодів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив метаданих про використання кеш-пам'яті опкодів або \*\*`false`\*\*в случае возникновения ошибки.

Масив, що повертається цією функцією, містить такі елементи:

-   `memory_total`\- Об'єм пам'яті в байтах, виділений для кеша опкодів.
-   `memory_free`\- Об'єм вільної пам'яті в байтах, доступної для кеша опкодів.
-   `num_used_blks`\- кількість блоків пам'яті, які використовуються кешем опкодів.
-   `num_free_blks`\- Кількість вільних блоків пам'яті, доступних для кешу опкодів.
-   `memory_overhead`\- Об'єм пам'яті в байтах, що використовується для внутрішніх структур кешу опкодів.

**Увага**

Ця функція *ВИДАЛЕНО* у PHP 7.0.0.

### Приклади

**Пример #1 Пример использования**wincache\_ocache\_meminfo()\*\*\*\*

```php
<pre>
<?php
print_r(wincache_ocache_meminfo());
?>
</pre>
```

Результат виконання наведеного прикладу:

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

-   [wincache\_fcache\_fileinfo()](function.wincache-fcache-fileinfo.md) \- Отримує інформацію про файли, закешовані у файловому кеші
-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_ucache\_info()](function.wincache-ucache-info.md) \- Отримує інформацію про дані, що зберігаються в кеші користувача
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
