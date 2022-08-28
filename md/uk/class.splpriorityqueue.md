Клас SplPriorityQueue

-   [« SplMinHeap::compare](splminheap.compare.html)
    
-   [SplPriorityQueue::compare »](splpriorityqueue.compare.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](spl.datastructures.html)
    
-   Клас SplPriorityQueue
    

# Клас SplPriorityQueue

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplPriorityQueue забезпечує основні функціональні можливості пріоритетної черги, реалізований за допомогою купи з максимальним елементом нагорі (max-heap).

> **Зауваження**: Порядок елементів з однаковим пріоритетом *не визначений*. Він може відрізнятись від порядку, в якому елементи були вставлені.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplPriorityQueue
     

     implements 
       Iterator,  Countable {

    /* Методы */
     
   public compare(mixed $priority1, mixed $priority2): int
public count(): int
public current(): mixed
public extract(): mixed
public getExtractFlags(): int
public insert(mixed $value, mixed $priority): bool
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

## Зміст

-   [SplPriorityQueue::compare](splpriorityqueue.compare.html) — Порівнює пріоритети для коректного розміщення елементів у чергу
-   [SplPriorityQueue::count](splpriorityqueue.count.html) — Здійснює підрахунок елементів у черзі
-   [SplPriorityQueue::current](splpriorityqueue.current.html) — Повертає вузол, на який вказує ітератор.
-   [SplPriorityQueue::extract](splpriorityqueue.extract.html) — Витягує вузол із початку черги і пересортує її.
-   [SplPriorityQueue::getExtractFlags](splpriorityqueue.getextractflags.html) — Отримати прапори вилучення
-   [SplPriorityQueue::insert](splpriorityqueue.insert.html) — Додає елемент у чергу та пересортує її
-   [SplPriorityQueue::isCorrupted](splpriorityqueue.iscorrupted.html) — Вказує, чи є пріоритетна черга у пошкодженому стані
-   [SplPriorityQueue::isEmpty](splpriorityqueue.isempty.html) — Перевіряє, чи черга є порожньою
-   [SplPriorityQueue::key](splpriorityqueue.key.html) — Повертає індекс поточного сайту
-   [SplPriorityQueue::next](splpriorityqueue.next.html) - Перехід до наступного вузла
-   [SplPriorityQueue::recoverFromCorruption](splpriorityqueue.recoverfromcorruption.html) - Відновлює коректний стан черги
-   [SplPriorityQueue::rewind](splpriorityqueue.rewind.html) - Перекладає ітератор на початок черги
-   [SplPriorityQueue::setExtractFlags](splpriorityqueue.setextractflags.html) — Встановлює режим вилучення вузлів
-   [SplPriorityQueue::top](splpriorityqueue.top.html) — Повертає вузол, що знаходиться на початку черги
-   [SplPriorityQueue::valid](splpriorityqueue.valid.html) — Перевіряє, чи є у черзі ще елементи