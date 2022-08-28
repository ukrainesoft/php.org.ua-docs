Сортування за допомогою заданої користувачем функції та збереження ключів

-   [« ArrayIterator::setFlags](arrayiterator.setflags.html)
    
-   [ArrayIterator::uksort »](arrayiterator.uksort.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayIterator](class.arrayiterator.html)
    
-   Сортування за допомогою заданої користувачем функції та збереження ключів
    

# ArrayIterator::uasort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::uasort — Сортування за допомогою заданої користувачем функції та збереження ключів

### Опис

```methodsynopsis
public ArrayIterator::uasort(callable $callback): bool
```

Сортує записи у масиві за значеннями, використовуючи функцію сортування, визначену користувачем та зберігаючи зв'язок ключ-значення.

> **Зауваження**
> 
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій початковий порядок. До PHP 8.0.0 їх відносний порядок у відсортованому масиві не було визначено.

### Список параметрів

`callback`

Функція порівняння повинна повертати ціле, яке менше, дорівнює чи більше нуля, якщо перший аргумент є відповідно меншим, рівним чи більшим, ніж другий.

```methodsynopsis
callback(mixed $a, mixed $b): int
```

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [ArrayIterator::asort()](arrayiterator.asort.html) - Сортує елементи за значеннями
-   [ArrayIterator::ksort()](arrayiterator.ksort.html) - Сортує елементи за ключами
-   [ArrayIterator::natcasesort()](arrayiterator.natcasesort.html) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort()](arrayiterator.natsort.html) - Сортує елементи "натурально"
-   [ArrayIterator::uksort()](arrayiterator.uksort.html) - Сортування за ключами за допомогою заданої функції порівняння
-   [uasort()](function.uasort.html) - Сортує масив, використовуючи функцію користувача для порівняння елементів зі збереженням ключів