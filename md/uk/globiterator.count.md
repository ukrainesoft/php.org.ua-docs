Визначає кількість директорій та файлів

-   [« GlobIterator::construct](globiterator.construct.html)
    
-   [InfiniteIterator »](class.infiniteiterator.html)
    
-   [PHP Manual](index.html)
    
-   [GlobIterator](class.globiterator.html)
    
-   Визначає кількість директорій та файлів
    

# GlobIterator::count

(PHP 5> = 5.3.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання **GlobIterator::count()****

```php
<?php
$iterator = new GlobIterator('*.xml');

printf("Найдено элементов: %d \r\n", $iterator->count());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Найдено элементов: 8
```

### Дивіться також

-   [GlobIterator::construct()](globiterator.construct.html) - створює ітератор директорії, використовуючи glob-вираз
-   [count()](function.count.html) - Підраховує кількість елементів масиву або Countable об'єкті
-   [glob()](function.glob.html) - Знаходить файлові шляхи, що збігаються із шаблоном