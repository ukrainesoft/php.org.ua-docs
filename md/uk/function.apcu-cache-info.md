---
navigation:
  - function.apcu-add.md: « apcu\_add
  - function.apcu-cas.md: apcu\_cas »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_cache\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_cache\_info

(PECL apcu >= 4.0.0)

apcu\_cache\_info — Витягує закешовану інформацію зі сховища APCu

### Опис

```methodsynopsis
apcu_cache_info(bool $limited = false): array|false
```

Витягує закешовану інформацію зі сховища APCu.

### Список параметрів

`limited`

Якщо `limited`задан как\*\*`true`\*\*, що повертається значення не міститиме індивідуальний список записів кеша. Це корисно під час спроб оптимізувати дзвінки для отримання статистики.

### Значення, що повертаються

Масив кешованих даних (і метадані) або \*\*`false`\*\*в случае возникновения ошибки

> **Зауваження** **apcu\_cache\_info()** Викликає попередження, якщо неможливо отримати дані кеша APC. Зазвичай це відбувається, якщо APC не дозволено.

### список змін

| Версия | Опис |
| --- | --- |
| PECL apcu 3.0.11 | Добавлен параметр`limited` |
| PECL apcu 3.0.16 | Додана опція "`filehits`для параметра `cache_type` |

### Приклади

**Пример #1 Пример использования**apcu\_cache\_info()\*\*\*\*

```php
<?php
print_r(apcu_cache_info());
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [Директиви конфігурації APCu](apcu.configuration.md)
-   [APCUIterator::getTotalSize()](apcuiterator.gettotalsize.md) \- Загальний розмір кешу
-   [APCUIterator::getTotalHits()](apcuiterator.gettotalhits.md) \- Отримати загальну кількість влучень у кеш
-   [APCUIterator::getTotalCount()](apcuiterator.gettotalcount.md) \- Отримати загальну кількість записів
