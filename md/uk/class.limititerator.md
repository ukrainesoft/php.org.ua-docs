---
navigation:
  - iteratoriterator.valid.md: '« IteratorIterator::valid'
  - limititerator.construct.md: 'LimitIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас LimitIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас LimitIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Класс**LimitIterator** дозволяє зробити перебір обмеженої кількості елементів у [Iterator](class.iterator.md)

## Огляд класів

```classsynopsis

    
     class LimitIterator
    

    
     extends
      IteratorIterator
     {

    /* Методы */
    
   public __construct(Iterator $iterator, int $offset = 0, int $limit = -1)

    public current(): mixed
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

**Приклад #1 Приклад використання** LimitIterator\*\*\*\*

```php
<?php

// Создать итератор для ограничения
$fruits = new ArrayIterator(array(
    'apple',
    'banana',
    'cherry',
    'damson',
    'elderberry'
));

// Цикл только по первым трём фруктам
foreach (new LimitIterator($fruits, 0, 3) as $fruit) {
    var_dump($fruit);
}

echo "\n";

// Цикл, начиная с третьего фрукта и до конца
// Примечание: смещение начинается с нуля для яблока
foreach (new LimitIterator($fruits, 2) as $fruit) {
    var_dump($fruit);
}

?>
```

Результат виконання наведеного прикладу:

```
string(5) "apple"
string(6) "banana"
string(6) "cherry"

string(6) "cherry"
string(6) "damson"
string(10) "elderberry"
```

## Зміст

-   [LimitIterator::\_\_construct](limititerator.construct.md) \- Конструктор класу LimitIterator
-   [LimitIterator::current](limititerator.current.md)— Отримання поточного елемента
-   [LimitIterator::getPosition](limititerator.getposition.md)— Повертає поточну позицію
-   [LimitIterator::key](limititerator.key.md)— Отримання поточного ключа
-   [LimitIterator::next](limititerator.next.md)— Переміщення до наступної позиції
-   [LimitIterator::rewind](limititerator.rewind.md)— Переміщує покажчик на початкову позицію
-   [LimitIterator::seek](limititerator.seek.md) \- Переміщає ітератор на задану позицію
-   [LimitIterator::valid](limititerator.valid.md) \- Перевіряє валідність поточного елемента
