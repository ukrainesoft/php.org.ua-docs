Витягує закешовану інформацію зі сховища APCu

-   [« apcuadd](function.apcu-add.html)
    
-   [apcucas »](function.apcu-cas.html)
    
-   [PHP Manual](index.html)
    
-   [Функции APCu](ref.apcu.html)
    
-   Витягує закешовану інформацію зі сховища APCu
    

# apcucacheinfo

(PECL apcu >= 4.0.0)

apcucacheinfo — Витягує закешовану інформацію зі сховища APCu

### Опис

```methodsynopsis
apcu_cache_info(bool $limited = false): array|false
```

Витягує закешовану інформацію зі сховища APCu.

### Список параметрів

`limited`

Якщо `limited` заданий як **`true`**, що повертається значення не міститиме індивідуальний список записів кеша. Це корисно під час спроб оптимізувати дзвінки для отримання статистики.

### Значення, що повертаються

Масив кешованих даних (і метадані) або **`false`** у разі виникнення помилки

> **Зауваження** **apcucacheinfo()** Викликає попередження, якщо неможливо отримати дані кеша APC. Зазвичай це відбувається, якщо APC не дозволено.

### список змін

| Версия           | Описание                                           |
|------------------|----------------------------------------------------|
| PECL apcu 3.0.11 | Доданий параметр `limited`                         |
| PECL apcu 3.0.16 | Додана опція "`filehits`для параметра `cache_type` |

### Приклади

**Приклад #1 Приклад використання **apcucacheinfo()****

```php
<?php
print_r(apcu_cache_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [num_slots] => 2000
    [ttl] => 0
    [num_hits] => 9
    [num_misses] => 3
    [start_time] => 1123958803
    [cache_list] => Array
        (
            [0] => Array
                (
                    [filename] => /path/to/apcu_test.php
                    [device] => 29954
                    [inode] => 1130511
                    [type] => file
                    [num_hits] => 1
                    [mtime] => 1123960686
                    [creation_time] => 1123960696
                    [deletion_time] => 0
                    [access_time] => 1123962864
                    [ref_count] => 1
                    [mem_size] => 677
                )
            [1] => Array (...итерирует для каждого закешированного файла)
)
```

### Дивіться також

-   [Директиви конфігурації APCu](apcu.configuration.html)
-   [APCUIterator::getTotalSize()](apcuiterator.gettotalsize.html) - Загальний розмір кешу
-   [APCUIterator::getTotalHits()](apcuiterator.gettotalhits.html) - Отримати загальну кількість влучень у кеш
-   [APCUIterator::getTotalCount()](apcuiterator.gettotalcount.html) - Отримати загальну кількість записів