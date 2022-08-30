Клас LimitIterator

-   [« IteratorIterator::valid](iteratoriterator.valid.html)
    
-   [LimitIterator::construct »](limititerator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ітератори](spl.iterators.html)
    
-   Клас LimitIterator
    

# Клас LimitIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Клас **LimitIterator** дозволяє зробити перебір обмеженої кількості елементів у [Iterator](class.iterator.html)

## Огляд класів

```classsynopsis

     
    

    
     
      class LimitIterator
     

     
      extends
       IteratorIterator
     
     {

    /* Методы */
    
   public __construct(Iterator $iterator, int $offset = 0, int $limit = -1)

    public current(): mixed
public getInnerIterator(): Iterator
public getPosition(): int
public key(): mixed
public next(): void
public rewind(): void
public seek(int $offset): int
public valid(): bool


    /* Наследуемые методы */
    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Приклади

**Приклад #1 Приклад використання **LimitIterator****

```php
<?php

// Создать итератор для ограничения
$fruits = new ArrayIterator(array(
    'apple',
    'banana',
    'cherry',
    'damson',
    'elderberry'
));

// Цикл только по первым трём фруктам
foreach (new LimitIterator($fruits, 0, 3) as $fruit) {
    var_dump($fruit);
}

echo "\n";

// Цикл, начиная с третьего фрукта и до конца
// Примечание: смещение начинается с нуля для яблока
foreach (new LimitIterator($fruits, 2) as $fruit) {
    var_dump($fruit);
}

?>
```

Результат виконання цього прикладу:

```
string(5) "apple"
string(6) "banana"
string(6) "cherry"

string(6) "cherry"
string(6) "damson"
string(10) "elderberry"
```

## Зміст

-   [LimitIterator::construct](limititerator.construct.html) - Конструктор класу LimitIterator
-   [LimitIterator::current](limititerator.current.html) — Отримання поточного елемента
-   [LimitIterator::getInnerIterator](limititerator.getinneriterator.html) — Отримання внутрішнього об'єкта-ітератора
-   [LimitIterator::getPosition](limititerator.getposition.html) — Повертає поточну позицію
-   [LimitIterator::key](limititerator.key.html) — Отримання поточного ключа
-   [LimitIterator::next](limititerator.next.html) — Переміщення до наступної позиції
-   [LimitIterator::rewind](limititerator.rewind.html) — Переміщує покажчик на початкову позицію
-   [LimitIterator::seek](limititerator.seek.html) - Переміщає ітератор на задану позицію
-   [LimitIterator::valid](limititerator.valid.html) - Перевіряє валідність поточного елемента