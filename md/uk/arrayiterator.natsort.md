Сортує елементи "натурально"

-   [« ArrayIterator::natcasesort](arrayiterator.natcasesort.html)
    
-   [ArrayIterator::next »](arrayiterator.next.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayIterator](class.arrayiterator.html)
    
-   Сортує елементи "натурально"
    

# ArrayIterator::natsort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::natsort — Сортує елементи "натурально"

### Опис

```methodsynopsis
public ArrayIterator::natsort(): bool
```

Сортує записи у масиві за значеннями, використовуючи алгоритм натурального сортування.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [ArrayIterator::asort()](arrayiterator.asort.html) - Сортує елементи за значеннями
-   [ArrayIterator::ksort()](arrayiterator.ksort.html) - Сортує елементи за ключами
-   **ArrayIterator::natsort()**
-   [ArrayIterator::uasort()](arrayiterator.uasort.html) - Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.html) - Сортування за ключами за допомогою заданої функції порівняння
-   [natsort()](function.natsort.html) - Сортує масив, використовуючи алгоритм "natural order"