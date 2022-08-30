Сортує елементи "натурально", з урахуванням регістру

-   [« ArrayIterator::ksort](arrayiterator.ksort.md)
    
-   [ArrayIterator::natsort »](arrayiterator.natsort.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayIterator](class.arrayiterator.md)
    
-   Сортує елементи "натурально", з урахуванням регістру
    

# ArrayIterator::natcasesort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::natcasesort — Сортує елементи "натурально", з урахуванням регістру

### Опис

```methodsynopsis
public ArrayIterator::natcasesort(): bool
```

Сортує записи у масиві за значеннями, використовуючи алгоритм натурального сортування з урахуванням регістру.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [ArrayIterator::asort()](arrayiterator.asort.md) - Сортує елементи за значеннями
-   [ArrayIterator::ksort()](arrayiterator.ksort.md) - Сортує елементи за ключами
-   [ArrayIterator::natsort()](arrayiterator.natsort.md) - Сортує елементи "натурально"
-   [ArrayIterator::uasort()](arrayiterator.uasort.md) - Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.md) - Сортування за ключами за допомогою заданої функції порівняння
-   [natcasesort()](function.natcasesort.md) - Сортує масив, використовуючи алгоритм "natural order" без урахування регістру символів