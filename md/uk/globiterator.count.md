---
navigation:
  - globiterator.construct.md: '« GlobIterator::\_\_construct'
  - class.infiniteiterator.md: InfiniteIterator »
  - index.md: PHP Manual
  - class.globiterator.md: GlobIterator
title: 'GlobIterator::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GlobIterator::count

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

GlobIterator::count — Визначає кількість директорій та файлів

### Опис

```methodsynopsis
public GlobIterator::count(): int
```

Визначає кількість директорій та файлів, що збігаються з glob-виразом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість директорій та файлів у вигляді цілого числа (int).

### Приклади

**Пример #1 Пример использования**GlobIterator::count()\*\*\*\*

```php
<?php
$iterator = new GlobIterator('*.xml');

printf("Найдено элементов: %d \r\n", $iterator->count());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Найдено элементов: 8
```

### Дивіться також

-   [GlobIterator::\_\_construct()](globiterator.construct.md) \- створює ітератор директорії, використовуючи glob-вираз
-   [count()](function.count.md) \- Підраховує кількість елементів масиву або Countable об'єкті
-   [glob()](function.glob.md) \- Знаходить файлові шляхи, що збігаються із шаблоном
