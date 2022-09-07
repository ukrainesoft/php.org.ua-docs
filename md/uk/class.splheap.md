---
navigation:
  - splqueue.setiteratormode.md: '« SplQueue::setIteratorMode'
  - splheap.compare.md: 'SplHeap::compare »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplHeap
---
# Клас SplHeap

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplHeap надає основні функціональні можливості купи.

## Огляд класів

```classsynopsis

     
    

    
     
      abstract
      class SplHeap
     

     implements 
       Iterator,  Countable {

    /* Методы */
     
   protected compare(mixed $value1, mixed $value2): int
public count(): int
public current(): mixed
public extract(): mixed
public insert(mixed $value): bool
public isCorrupted(): bool
public isEmpty(): bool
public key(): int
public next(): void
public recoverFromCorruption(): bool
public rewind(): void
public top(): mixed
public valid(): bool

    }
```

## Зміст

-   [SplHeap::compare](splheap.compare.md) — Порівнює елементи, щоб під час сортування коректно розмістити їх у купі
-   [SplHeap::count](splheap.count.md) — Визначає кількість елементів у купі
-   [SplHeap::current](splheap.current.md) — Повертає вузол, на який вказує ітератор.
-   [SplHeap::extract](splheap.extract.md) — Витягує вузол із купи і пересортує її.
-   [SplHeap::insert](splheap.insert.md) — Вставляє елемент у купу та пересортує її
-   [SplHeap::isCorrupted](splheap.iscorrupted.md) — Вказує, чи купа у пошкодженому стані
-   [SplHeap::isEmpty](splheap.isempty.md) — Перевірка, чи пуста купа
-   [SplHeap::key](splheap.key.md) — Повертає індекс поточного сайту
-   [SplHeap::next](splheap.next.md) - Перехід до наступного вузла
-   [SplHeap::recoverFromCorruption](splheap.recoverfromcorruption.md) - Відновлює коректний стан купи
-   [SplHeap::rewind](splheap.rewind.md) - Переклад ітератора на початок
-   [SplHeap::top](splheap.top.md) - Повертає вузол, що знаходиться на вершині купи
-   [SplHeap::valid](splheap.valid.md) - Перевіряє, чи містить купа ще елементи
