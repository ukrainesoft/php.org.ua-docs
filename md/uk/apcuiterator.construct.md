---
navigation:
  - class.apcuiterator.md: « APCUIterator
  - apcuiterator.current.md: 'APCUIterator::current »'
  - index.md: PHP Manual
  - class.apcuiterator.md: APCUIterator
title: 'APCUIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# APCUIterator::\_\_construct

(PECL apcu >= 5.0.0)

APCUIterator::\_\_construct — Створює об'єкт ітератора класу APCUIterator

### Опис

public**APCUIterator::\_\_construct**  
array|string|null`$search` **`null`**,  
int`$format`\= APC\_ITER\_ALL,  
int`$chunk_size`  
int`$list`\= APC\_LIST\_ACTIVE  
) .

Створює об'єкт [APCUIterator](class.apcuiterator.md)

### Список параметрів

`search`

Або регулярне вираження [PCRE](book.pcre.md)що відповідає іменам ключів APCu, заданим як рядки (string). Або масив (array) рядків (string) із іменами ключів APCu. Або, необов'язково, **`null`** щоб пропустити пошук.

`format`

Формат, заданий однією з констант [APC\_ITER\_\*](apcu.constants.md)

`chunk_size`

Розмір блоку даних. Має бути більше 0. За замовчуванням 100.

`list`

Тип списку. Задається константами **`APC_LIST_ACTIVE`**или**`APC_LIST_DELETED`**

### Приклади

**Пример #1 Пример использования**APCUIterator::\_\_construct()\*\*\*\*

```php
<?php
foreach (new APCUIterator('/^counter\./') as $counter) {
    echo "$counter[key]: $counter[value]\n";
    apc_dec($counter['key'], $counter['value']);
}
?>
```

### Дивіться також

-   [apcu\_exists()](function.apcu-exists.md) \- Перевіряє, чи існують записи
-   [apcu\_cache\_info()](function.apcu-cache-info.md) \- Витягує закешовану інформацію зі сховища APCu
