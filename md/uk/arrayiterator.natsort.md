---
navigation:
  - arrayiterator.natcasesort.md: '« ArrayIterator::natcasesort'
  - arrayiterator.next.md: 'ArrayIterator::next »'
  - index.md: PHP Manual
  - class.arrayiterator.md: ArrayIterator
title: 'ArrayIterator::natsort'
---
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

-   [ArrayIterator::asort()](arrayiterator.asort.md) - Сортує елементи за значеннями
-   [ArrayIterator::ksort()](arrayiterator.ksort.md) - Сортує елементи за ключами
-   **ArrayIterator::natsort()**
-   [ArrayIterator::uasort()](arrayiterator.uasort.md) - Сортування за допомогою заданої користувачем функції та збереженням ключів
-   [ArrayIterator::uksort()](arrayiterator.uksort.md) - Сортування за ключами за допомогою заданої функції порівняння
-   [natsort()](function.natsort.md) - Сортує масив, використовуючи алгоритм "natural order"
