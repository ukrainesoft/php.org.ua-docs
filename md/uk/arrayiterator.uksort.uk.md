Сортування за ключами за допомогою функції порівняння

-   [« ArrayIterator::uasort](arrayiterator.uasort.md)
    
-   [ArrayIterator::unserialize »](arrayiterator.unserialize.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayIterator](class.arrayiterator.md)
    
-   Сортування за ключами за допомогою функції порівняння
    

# ArrayIterator::uksort

(PHP 5> = 5.2.0, PHP 7, PHP 8)

ArrayIterator::uksort — Сортування за ключами за допомогою заданої функції порівняння

### Опис

```methodsynopsis
public ArrayIterator::uksort(callable $callback): bool
```

Сортує записи у масиві за ключами, використовуючи функцію сортування, визначену користувачем.

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

-   [ArrayIterator::asort()](arrayiterator.asort.md) - Сортує елементи за значеннями
-   [ArrayIterator::ksort()](arrayiterator.ksort.md) - Сортує елементи за ключами
-   [ArrayIterator::natcasesort()](arrayiterator.natcasesort.md) - Сортує елементи "натурально", з урахуванням регістру
-   [ArrayIterator::natsort()](arrayiterator.natsort.md) - Сортує елементи "натурально"
-   **ArrayIterator::uksort()**
-   [uksort()](function.uksort.md) - Сортує масив за ключами, використовуючи функцію користувача для порівняння ключів