Клас SplHeap

-   [« SplQueue::setIteratorMode](splqueue.setiteratormode.html)
    
-   [SplHeap::compare »](splheap.compare.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](spl.datastructures.html)
    
-   Клас SplHeap
    

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

-   [SplHeap::compare](splheap.compare.html) — Порівнює елементи, щоб під час сортування коректно розмістити їх у купі
-   [SplHeap::count](splheap.count.html) — Визначає кількість елементів у купі
-   [SplHeap::current](splheap.current.html) — Повертає вузол, на який вказує ітератор.
-   [SplHeap::extract](splheap.extract.html) — Витягує вузол із купи і пересортує її.
-   [SplHeap::insert](splheap.insert.html) — Вставляє елемент у купу та пересортує її
-   [SplHeap::isCorrupted](splheap.iscorrupted.html) — Вказує, чи купа у пошкодженому стані
-   [SplHeap::isEmpty](splheap.isempty.html) — Перевірка, чи пуста купа
-   [SplHeap::key](splheap.key.html) — Повертає індекс поточного сайту
-   [SplHeap::next](splheap.next.html) - Перехід до наступного вузла
-   [SplHeap::recoverFromCorruption](splheap.recoverfromcorruption.html) - Відновлює коректний стан купи
-   [SplHeap::rewind](splheap.rewind.html) - Переклад ітератора на початок
-   [SplHeap::top](splheap.top.html) - Повертає вузол, що знаходиться на вершині купи
-   [SplHeap::valid](splheap.valid.html) - Перевіряє, чи містить купа ще елементи