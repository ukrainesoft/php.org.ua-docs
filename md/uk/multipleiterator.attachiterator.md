Приєднує ітератор

-   [« MultipleIterator](class.multipleiterator.html)
    
-   [MultipleIterator::construct »](multipleiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MultipleIterator](class.multipleiterator.html)
    
-   Приєднує ітератор
    

# MultipleIterator::attachIterator

(PHP 5> = 5.3.0, PHP 7, PHP 8)

MultipleIterator::attachIterator — Приєднує ітератор

### Опис

```methodsynopsis
public MultipleIterator::attachIterator(Iterator $iterator, string|int|null $info = null): void
```

Приєднує ітератор.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`iterator`

Новий ітератор для приєднання.

`info`

Асоціативна інформація для ітератора (Iterator), яка має бути представлена ​​цілим числом (int), рядком (string), або **`null`**

### Значення, що повертаються

Опис...

### Помилки

**IlegallegalValueException**, якщо параметр `iterator` недійсний, або якщо `info` містить асоційовану інформацію.

### Дивіться також

-   [MultipleIterator::construct()](multipleiterator.construct.html) - Створює новий MultipleIterator