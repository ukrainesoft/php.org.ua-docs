---
navigation:
  - function.apcu-dec.md: « apcu\_dec
  - function.apcu-enabled.md: apcu\_enabled »
  - index.md: PHP Manual
  - ref.apcu.md: Функції APCu
title: apcu\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apcu\_delete

(PECL apcu >= 4.0.0)

apcu\_delete — Видалення збереженого значення з кешу.

### Опис

```methodsynopsis
apcu_delete(mixed $key): mixed
```

Видаляє збережене значення з кеша.

### Список параметрів

`key`

`key` можна встановити як рядок, для видалення одного значення, або як масив рядків, для видалення кількох значень, або як об'єкт [APCUIterator](class.apcuiterator.md)

### Значення, що повертаються

Якщо `key` є масивом (array), повертається індексований масив (array) ключів. В іншому випадку повертається **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** apcu\_delete()\*\*\*\*

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

-   [apcu\_store()](function.apcu-store.md) \- Кешує змінну
-   [apcu\_fetch()](function.apcu-fetch.md) \- Витягує з кеша збережену змінну
-   [apcu\_clear\_cache()](function.apcu-clear-cache.md) \- Очистити кеш APCu
-   [APCUIterator](class.apcuiterator.md)
