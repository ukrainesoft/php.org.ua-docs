Отримує інформацію про дані, що зберігаються в кеші користувача

-   [« wincacheucacheinc](function.wincache-ucache-inc.html)
    
-   [wincacheucachememinfo »](function.wincache-ucache-meminfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции WinCache](ref.wincache.html)
    
-   Отримує інформацію про дані, що зберігаються в кеші користувача
    

# wincacheucacheinfo

(PECL wincache >= 1.1.0)

wincacheucacheinfo — Отримує інформацію про дані, що зберігаються в кеші користувача.

### Опис

```methodsynopsis
wincache_ucache_info(bool $summaryonly = false, string $key = NULL): array|false
```

Отримує інформацію про дані, що зберігаються в кеші користувача.

### Список параметрів

`summaryonly`

Визначає, чи буде масив, що повертається, містити інформацію про окремі записи кеша разом зі зведенням користувальницького кешу.

`key`

Ключ запису в кеші користувача. Якщо зазначено, то масив, що повертається, міститиме інформацію тільки про цей запис кеша. Якщо не вказано і для `summaryonly` встановлено значення **`false`**, тоді масив, що повертається, міститиме інформацію про всі записи кеша.

### Значення, що повертаються

Масив метаданих про використання користувальницького кешу або **`false`** у разі виникнення помилки

Масив, що повертається цією функцією, містить такі елементи:

-   `total_cache_uptime` - загальний час в секундах, протягом якого кеш був активний.
    
-   `total_item_count` - загальна кількість елементів, які в даний момент знаходяться в кеші користувача.
    
-   `is_local_cache` - true - метадані кеша призначені для екземпляра локального кешу, false, якщо метадані призначені для глобального кешу.
    
-   `total_hit_count` - кількість разів, коли дані було отримано з кешу.
    
-   `total_miss_count` - кількість разів, коли дані не знайшли в кеші.
    
-   `ucache_entries` - масив, що містить інформацію про всі кешовані елементи:
    
    -   `key_name` - Ім'я ключа, який використовується для зберігання даних.
    -   `value_type` - Тип значення, що зберігається ключем.
    -   `use_time` - час у секундах із моменту звернення до файлу в кеші опкодів.
    -   `last_check` - час у секундах із моменту перевірки файлу на наявність модифікацій.
    -   `is_session` - Вказує, чи є дані змінної сесії.
    -   `ttl_seconds` - час, що залишився для даних, щоб перебувати в кеші, означає 0 нескінченність.
    -   `age_seconds` - час, що минув з моменту додавання даних у кеш.
    -   `hitcount` - кількість разів, коли дані було отримано з кешу.

### Приклади

**Приклад #1 Приклад використання **wincacheucacheinfo()****

```php
<?php
wincache_ucache_get('green');
wincache_ucache_set('green', 2922);
wincache_ucache_get('green');
wincache_ucache_get('green');
wincache_ucache_get('green');
print_r(wincache_ucache_info());
?>
```

Результат виконання цього прикладу:

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

-   [wincachefcachememinfo()](function.wincache-fcache-meminfo.html) - Отримує інформацію про використання пам'яті файлового кешу
-   [wincacheocachefileinfo()](function.wincache-ocache-fileinfo.html) - Отримує інформацію про файли, закешовані в кеші опкодів
-   [wincacheocachememinfo()](function.wincache-ocache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті опкодів
-   [wincacherplistmeminfo()](function.wincache-rplist-meminfo.html) - Отримує інформацію про використання пам'яті за допомогою кеша шляху до файлу роздільної здатності
-   [wincacherplistfileinfo()](function.wincache-rplist-fileinfo.html) - Отримує інформацію про дозвіл кешу шляху до файлу дозволу
-   [wincacherefreshіфchanged()](function.wincache-refresh-if-changed.html) - Оновлює записи кеша для закешованих файлів
-   [wincacheucachememinfo()](function.wincache-ucache-meminfo.html) - Отримує інформацію про використання пам'яті кешу користувача.
-   [wincachescacheinfo()](function.wincache-scache-info.html) - Отримує інформацію про файли, закешовані в кеші сесії
-   [wincachescachememinfo()](function.wincache-scache-meminfo.html) - Отримує інформацію про використання кеш-пам'яті сесії