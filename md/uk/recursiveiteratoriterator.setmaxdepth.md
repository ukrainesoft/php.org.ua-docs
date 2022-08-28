Встановлення максимальної глибини вкладеності

-   [« RecursiveIteratorIterator::rewind](recursiveiteratoriterator.rewind.html)
    
-   [RecursiveIteratorIterator::valid »](recursiveiteratoriterator.valid.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveIteratorIterator](class.recursiveiteratoriterator.html)
    
-   Встановлення максимальної глибини вкладеності
    

# RecursiveIteratorIterator::setMaxDepth

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveIteratorIterator::setMaxDepth — Встановлення максимальної глибини вкладеності

### Опис

```methodsynopsis
public RecursiveIteratorIterator::setMaxDepth(int $maxDepth = -1): void
```

Задає максимальну глибину вкладеності елементів.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`maxDepth`

Максимально допустима глибина вкладеності . `-1` знімає обмеження на глибину рекурсії.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [Exception](class.exception.html), якщо аргумент `maxDepth` менше `-1`