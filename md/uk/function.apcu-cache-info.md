- [«apcu_add](function.apcu-add.md)
- [apcu_cas »](function.apcu-cas.md)

- [PHP Manual](index.md)
- [Функції APCu](ref.apcu.md)
- Виймає закешовану інформацію зі сховища APCu

#apcu_cache_info

(PECL apcu \>= 4.0.0)

apcu_cache_info — Витягує закешовану інформацію зі сховища APCu

### Опис

**apcu_cache_info**(bool `$limited` = **`false`**): array\|false

Витягує закешовану інформацію зі сховища APCu.

### Список параметрів

`limited`
Якщо `limited` заданий як **`true`**, значення, що повертається, не буде
містити індивідуальний список записів кеша. Це корисно при спробах
оптимізувати дзвінки для отримання статистики.

### Значення, що повертаються

Масив кешованих даних (і метадані) або **`false`** у разі
виникнення помилки

> **Примітка**: **apcu_cache_info()** викликає попередження, якщо
> Неможливо отримати дані кеша APC. Зазвичай це відбувається, якщо APC
> не дозволено.

### Список змін

| Версія                                                             | Опис                      |
| ------------------------------------------------------------------ | ------------------------- |
| PECL APCU 3.0.11                                                   | Доданий параметр limited. |
| PECL apcu 3.0.16 Додано опцію "filehits" для параметра cache_type. |                           |

### Приклади

**Приклад #1 Приклад використання **apcu_cache_info()****

` <?phpprint_r(apcu_cache_info());?> `

Результатом виконання цього прикладу буде щось подібне:

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
[1] => Array (...ітерує для кожного закешованого файлу)
)

### Дивіться також

- [Директиви конфігурації APCu](apcu.configuration.md)
- [APCUIterator::getTotalSize()](apcuiterator.gettotalsize.md) -
Загальний розмір кешу
- [APCUIterator::getTotalHits()](apcuiterator.gettotalhits.md) -
Отримати загальну кількість влучень у кеш
- [APCUIterator::getTotalCount()](apcuiterator.gettotalcount.md) -
Отримати загальну кількість записів
