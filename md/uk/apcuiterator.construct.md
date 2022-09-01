---
navigation:
  - class.apcuiterator.md: « APCUIterator
  - apcuiterator.current.md: 'APCUIterator::current »'
  - index.md: PHP Manual
  - class.apcuiterator.md: APCUIterator
title: 'APCUIterator::construct'
---
# APCUIterator::construct

(PECL apcu >= 5.0.0)

APCUIterator::construct — Створює об'єкт ітератора класу APCUIterator

### Опис

public **APCUIterator::construct**  
array|string|null `$search` **`null`**  
int `$format` = APCITERALL,  
int `$chunk_size`  
int `$list` = APCLISTACTIVE

Створює об'єкт [APCUIterator](class.apcuiterator.md)

### Список параметрів

`search`

Або регулярне вираження [PCRE](book.pcre.md)що відповідає іменам ключів APCu, заданим як рядки (string). Або масив (array) рядків (string) із іменами ключів APCu. Або, необов'язково, **`null`** щоб пропустити пошук.

`format`

Формат, заданий однією з констант [APCITER](apcu.constants.md)

`chunk_size`

Розмір блоку даних. Має бути більше 0. За замовчуванням 100.

`list`

Тип списку. Задається константами **`APC_LIST_ACTIVE`** або **`APC_LIST_DELETED`**

### Приклади

**Приклад #1 Приклад використання **APCUIterator::construct()****

```php
<?php
foreach (new APCUIterator('/^counter\./') as $counter) {
    echo "$counter[key]: $counter[value]\n";
    apc_dec($counter['key'], $counter['value']);
}
?>
```

### Дивіться також

-   [apcuexists()](function.apcu-exists.md) - Перевіряє, чи існують записи
-   [apcucacheinfo()](function.apcu-cache-info.md) - Витягує закешовану інформацію зі сховища APCu
