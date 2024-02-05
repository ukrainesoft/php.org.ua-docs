---
navigation:
  - splminheap.compare.md: '« SplMinHeap::compare'
  - splpriorityqueue.compare.md: 'SplPriorityQueue::compare »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplPriorityQueue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplPriorityQueue

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplPriorityQueue забезпечує основні функціональні можливості пріоритетної черги, реалізований за допомогою купи з максимальним елементом нагорі (max-heap).

> **Зауваження**: Порядок елементів з однаковим пріоритетом *не визначений*. Він може відрізнятись від порядку, в якому елементи були вставлені.

## Огляд класів

```classsynopsis

    
     class SplPriorityQueue
    

    
     implements
      Iterator,

     Countable {

    /* Константы */
    
     public
     const
     int
      EXTR_BOTH;

    public
     const
     int
      EXTR_PRIORITY;

    public
     const
     int
      EXTR_DATA;


    /* Методы */
    
   public compare(mixed $priority1, mixed $priority2): int
public count(): int
public current(): mixed
public extract(): mixed
public getExtractFlags(): int
public insert(mixed $value, mixed $priority): true
public isCorrupted(): bool
public isEmpty(): bool
public key(): int
public next(): void
public recoverFromCorruption(): bool
public rewind(): void
public setExtractFlags(int $flags): int
public top(): mixed
public valid(): bool

   }
```

## Обумовлені константи

**`SplPriorityQueue::EXTR_BOTH`**

**`SplPriorityQueue::EXTR_PRIORITY`**

**`SplPriorityQueue::EXTR_DATA`**

## Зміст

-   [SplPriorityQueue::compare](splpriorityqueue.compare.md)— Порівнює пріоритети для коректного розміщення елементів у чергу
-   [SplPriorityQueue::count](splpriorityqueue.count.md)— Здійснює підрахунок елементів у черзі
-   [SplPriorityQueue::current](splpriorityqueue.current.md)— Повертає вузол, на який вказує ітератор.
-   [SplPriorityQueue::extract](splpriorityqueue.extract.md)— Витягує вузол із початку черги і пересортує її.
-   [SplPriorityQueue::getExtractFlags](splpriorityqueue.getextractflags.md)— Отримати прапори вилучення
-   [SplPriorityQueue::insert](splpriorityqueue.insert.md)— Додає елемент у чергу та пересортує її
-   [SplPriorityQueue::isCorrupted](splpriorityqueue.iscorrupted.md)— Вказує, чи є пріоритетна черга у пошкодженому стані
-   [SplPriorityQueue::isEmpty](splpriorityqueue.isempty.md)— Перевіряє, чи черга є порожньою
-   [SplPriorityQueue::key](splpriorityqueue.key.md)— Повертає індекс поточного сайту
-   [SplPriorityQueue::next](splpriorityqueue.next.md) \- Перехід до наступного вузла
-   [SplPriorityQueue::recoverFromCorruption](splpriorityqueue.recoverfromcorruption.md) \- Відновлює коректний стан черги
-   [SplPriorityQueue::rewind](splpriorityqueue.rewind.md)— перекладає ітератор на початок черги
-   [SplPriorityQueue::setExtractFlags](splpriorityqueue.setextractflags.md)— Встановлює режим вилучення вузлів
-   [SplPriorityQueue::top](splpriorityqueue.top.md)— Повертає вузол, що знаходиться на початку черги
-   [SplPriorityQueue::valid](splpriorityqueue.valid.md)— Перевіряє, чи є у черзі ще елементи
