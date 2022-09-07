---
navigation:
  - function.apcu-dec.md: « apcudec
  - function.apcu-enabled.md: apcuenabled »
  - index.md: PHP Manual
  - ref.apcu.md: Функции APCu
title: apcudelete
---
# apcudelete

(PECL apcu >= 4.0.0)

apcudelete — Видалення збереженого значення з кешу

### Опис

```methodsynopsis
apcu_delete(mixed $key): mixed
```

Видаляє збережене значення з кеша.

### Список параметрів

`key`

`key` можна встановити як рядок, для видалення одного значення, або як масив рядків, для видалення кількох значень, або як об'єкт [APCUIterator](class.apcuiterator.md)

### Значення, що повертаються

Якщо `key` є масивом (array), повертається індексований масив (array) ключів. В іншому випадку повертається **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **apcudelete()****

```php
<?php
$bar = 'BAR';
apcu_store('foo', $bar);

//Удаляем одну запись.
apcu_delete('foo');

// Удаляем несколько записей.
apcu_delete(['foo', 'bar', 'baz']);

// Используем итератор с регулярным выражением.
apcu_delete(new APCUIterator('#^myprefix_#'));
?>
```

### Дивіться також

-   [apcustore()](function.apcu-store.md) - Кешує змінну
-   [apcufetch()](function.apcu-fetch.md) - Витягує з кеша збережену змінну
-   [apcuclearcache()](function.apcu-clear-cache.md) - Очистити кеш APCu
-   [APCUIterator](class.apcuiterator.md)
