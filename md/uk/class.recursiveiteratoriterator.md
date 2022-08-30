Клас RecursiveIteratorIterator

-   [« RecursiveFilterIterator::hasChildren](recursivefilteriterator.haschildren.md)
    
-   [RecursiveIteratorIterator::beginChildren »](recursiveiteratoriterator.beginchildren.md)
    
-   [PHP Manual](index.md)
    
-   [Ітератори](spl.iterators.md)
    
-   Клас RecursiveIteratorIterator
    

# Клас RecursiveIteratorIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Може використовуватися для перебору рекурсивних ітераторів.

## Огляд класів

```classsynopsis

     
    

    
     
      class RecursiveIteratorIterator
     

     implements 
       OuterIterator {

    /* Константы */
    
     const
     int
      LEAVES_ONLY = 0;

    const
     int
      SELF_FIRST = 1;

    const
     int
      CHILD_FIRST = 2;

    const
     int
      CATCH_GET_CHILD = 16;


    /* Методы */
    
   public __construct(Traversable $iterator, int $mode = RecursiveIteratorIterator::LEAVES_ONLY, int $flags = 0)

    public beginChildren(): void
public beginIteration(): void
public callGetChildren(): ?RecursiveIterator
public callHasChildren(): bool
public current(): mixed
public endChildren(): void
public endIteration(): void
public getDepth(): int
public getInnerIterator(): RecursiveIterator
public getMaxDepth(): int|false
public getSubIterator(?int $level = null): ?RecursiveIterator
public key(): mixed
public next(): void
public nextElement(): void
public rewind(): void
public setMaxDepth(int $maxDepth = -1): void
public valid(): bool

   }
```

## Обумовлені константи

**`RecursiveIteratorIterator::LEAVES_ONLY`**

**`RecursiveIteratorIterator::SELF_FIRST`**

**`RecursiveIteratorIterator::CHILD_FIRST`**

**`RecursiveIteratorIterator::CATCH_GET_CHILD`**

## Зміст

-   [RecursiveIteratorIterator::beginChildren](recursiveiteratoriterator.beginchildren.md) — Перехід до першого дочірнього елемента
-   [RecursiveIteratorIterator::beginIteration](recursiveiteratoriterator.beginiteration.md) - Початок ітерації
-   [RecursiveIteratorIterator::callGetChildren](recursiveiteratoriterator.callgetchildren.md) — Отримання дочірніх елементів
-   [RecursiveIteratorIterator::callHasChildren](recursiveiteratoriterator.callhaschildren.md) — Перевірка, чи має елемент дочірні елементи
-   [RecursiveIteratorIterator::construct](recursiveiteratoriterator.construct.md) - Конструктор класу RecursiveIteratorIterator
-   [RecursiveIteratorIterator::current](recursiveiteratoriterator.current.md) — Отримує значення поточного елемента
-   [RecursiveIteratorIterator::endChildren](recursiveiteratoriterator.endchildren.md) — Закінчення дочірніх елементів
-   [RecursiveIteratorIterator::endIteration](recursiveiteratoriterator.enditeration.md) - Закінчення ітерації
-   [RecursiveIteratorIterator::getDepth](recursiveiteratoriterator.getdepth.md) - Визначає поточну глибину рекурсії
-   [RecursiveIteratorIterator::getInnerIterator](recursiveiteratoriterator.getinneriterator.md) — Отримання посилання на внутрішній ітератор
-   [RecursiveIteratorIterator::getMaxDepth](recursiveiteratoriterator.getmaxdepth.md) - Отримання максимальної глибини рекурсії
-   [RecursiveIteratorIterator::getSubIterator](recursiveiteratoriterator.getsubiterator.md) — Отримання активного вкладеного ітератора
-   [RecursiveIteratorIterator::key](recursiveiteratoriterator.key.md) — Отримання ключа поточного елемента
-   [RecursiveIteratorIterator::next](recursiveiteratoriterator.next.md) — Переміщення ітератора до наступного елементу
-   [RecursiveIteratorIterator::nextElement](recursiveiteratoriterator.nextelement.md) - Наступний елемент
-   [RecursiveIteratorIterator::rewind](recursiveiteratoriterator.rewind.md) — Переміщує ітератор на перший елемент верхнього рівня вкладеності внутрішнього ітератора
-   [RecursiveIteratorIterator::setMaxDepth](recursiveiteratoriterator.setmaxdepth.md) - Встановлення максимальної глибини вкладеності
-   [RecursiveIteratorIterator::valid](recursiveiteratoriterator.valid.md) - Перевірка допустимості поточної позиції