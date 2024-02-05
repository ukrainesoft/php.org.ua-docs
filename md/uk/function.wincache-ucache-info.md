---
navigation:
  - function.wincache-ucache-inc.md: « wincache\_ucache\_inc
  - function.wincache-ucache-meminfo.md: wincache\_ucache\_meminfo »
  - index.md: PHP Manual
  - ref.wincache.md: Функції WinCache
title: wincache\_ucache\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wincache\_ucache\_info

(PECL wincache >= 1.1.0)

wincache\_ucache\_info — Отримує інформацію про дані, що зберігаються в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_info(bool $summaryonly = false, string $key = NULL): array|false
```

Отримує інформацію про дані, що зберігаються в кеші користувача.

### Список параметрів

`summaryonly`

Визначає, чи буде масив, що повертається, містити інформацію про окремі записи кеша разом зі зведенням користувальницького кешу.

`key`

Ключ запису в кеші користувача. Якщо зазначено, то масив, що повертається, міститиме інформацію тільки про цей запис кеша. Якщо не вказано і для `summaryonly`установлено значение\*\*`false`\*\*, тоді масив, що повертається, міститиме інформацію про всі записи кеша.

### Значення, що повертаються

Масив метаданих про використання користувальницького кешу або \*\*`false`\*\*в случае возникновения ошибки

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime`\- загальний час у секундах, протягом якого кеш був активний.
    
-   `total_item_count`\- загальна кількість елементів, які в даний момент знаходяться в кеші користувача.
    
-   `is_local_cache`\- true - метадані кеша призначені для екземпляра локального кешу, false, якщо метадані призначені для глобального кешу.
    
-   `total_hit_count`\- кількість разів, коли дані було отримано з кешу.
    
-   `total_miss_count`\- кількість разів, коли дані не знайшли в кеші.
    
-   `ucache_entries`\- масив, що містить інформацію про всі кешовані елементи:
    
    -   `key_name`\- Ім'я ключа, який використовується для зберігання даних.
    -   `value_type`\- Тип значення, що зберігається ключем.
    -   `use_time`\- час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check`\- час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `is_session`\- Вказує, чи є дані змінної сесії.
    -   `ttl_seconds`\- час, що залишився для даних, щоб перебувати в кеші, 0 означає нескінченність.
    -   `age_seconds`\- час, що минув з моменту додавання даних у кеш.
    -   `hitcount`\- кількість разів, коли дані було отримано з кешу.

### Приклади

**Пример #1 Пример использования**wincache\_ucache\_info()\*\*\*\*

```php
<?php
wincache_ucache_get('green');
wincache_ucache_set('green', 2922);
wincache_ucache_get('green');
wincache_ucache_get('green');
wincache_ucache_get('green');
print_r(wincache_ucache_info());
?>
```

Результат виконання наведеного прикладу:

```
Array
( ["total_cache_uptime"] => int(0)
  ["is_local_cache"] => bool(false)
  ["total_item_count"] => int(1)
  ["total_hit_count"] => int(3)
  ["total_miss_count"] => int(1)
  ["ucache_entries"] => Array(1)
    ( [1] => Array(6)
      (
        ["key_name"] => string(5) "green"
        ["value_type"] => string(4) "long"
        ["is_session"] => int(0)
        ["ttl_seconds"] => int(0)
        ["age_seconds"] => int(0)
        ["hitcount"] => int(3)
       )
    )
)
```

### Дивіться також

-   [wincache\_fcache\_meminfo()](function.wincache-fcache-meminfo.md) \- Отримує інформацію про використання пам'яті файлового кешу
-   [wincache\_ocache\_fileinfo()](function.wincache-ocache-fileinfo.md) \- Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincache\_ocache\_meminfo()](function.wincache-ocache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincache\_rplist\_meminfo()](function.wincache-rplist-meminfo.md) \- Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincache\_rplist\_fileinfo()](function.wincache-rplist-fileinfo.md) \- Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincache\_refresh\_if\_changed()](function.wincache-refresh-if-changed.md) \- Оновлює записи кеша для закешованих файлів
-   [wincache\_ucache\_meminfo()](function.wincache-ucache-meminfo.md) \- Отримує інформацію про використання пам'яті кешу користувача.
-   [wincache\_scache\_info()](function.wincache-scache-info.md) \- Отримує інформацію про файли, закешовані в кеші сесії
-   [wincache\_scache\_meminfo()](function.wincache-scache-meminfo.md) \- Отримує інформацію про використання кеш-пам'яті сесії
