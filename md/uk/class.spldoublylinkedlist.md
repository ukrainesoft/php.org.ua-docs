Клас SplDoublyLinkedList

-   [« Структуры данных](spl.datastructures.html)
    
-   [SplDoublyLinkedList::add »](spldoublylinkedlist.add.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](spl.datastructures.html)
    
-   Клас SplDoublyLinkedList
    

# Клас SplDoublyLinkedList

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplDoublyLinkedList забезпечує основні функціональні можливості двозв'язкового списку.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplDoublyLinkedList
     

     implements 
       Iterator,  Countable,  ArrayAccess,  Serializable {

    /* Константы */
    
     const
     int
      IT_MODE_LIFO = 2;

    const
     int
      IT_MODE_FIFO = 0;

    const
     int
      IT_MODE_DELETE = 1;

    const
     int
      IT_MODE_KEEP = 0;


    /* Методы */
    
   public add(int $index, mixed $value): void
public bottom(): mixed
public count(): int
public current(): mixed
public getIteratorMode(): int
public isEmpty(): bool
public key(): int
public next(): void
public offsetExists(int $index): bool
public offsetGet(int $index): mixed
public offsetSet(?int $index, mixed $value): void
public offsetUnset(int $index): void
public pop(): mixed
public prev(): void
public push(mixed $value): void
public rewind(): void
public serialize(): string
public setIteratorMode(int $mode): int
public shift(): mixed
public top(): mixed
public unserialize(string $data): void
public unshift(mixed $value): void
public valid(): bool

   }
```

## Обумовлені константи

## Напрямок ітерації

**`SplDoublyLinkedList::IT_MODE_LIFO`**

Список повторюватиметься по порядку "останнім прийшов - першим вийшов", як стек.

**`SplDoublyLinkedList::IT_MODE_FIFO`**

Список повторюватиметься по порядку "першим прийшов - першим вийшов", як черга.

## Поведінка ітерації

**`SplDoublyLinkedList::IT_MODE_DELETE`**

Ітерація видалить повторювані елементи.

**`SplDoublyLinkedList::IT_MODE_KEEP`**

Ітерація не видаляє повторювані елементи.

## Зміст

-   [SplDoublyLinkedList::add](spldoublylinkedlist.add.html) — Додає/вставляє нове значення за вказаним індексом
-   [SplDoublyLinkedList::bottom](spldoublylinkedlist.bottom.html) - Отримує вузол, що знаходиться на початку двозв'язкового списку
-   [SplDoublyLinkedList::count](spldoublylinkedlist.count.html) - Підраховує кількість елементів у двозв'язному списку
-   [SplDoublyLinkedList::current](spldoublylinkedlist.current.html) — Повертає поточний елемент масиву
-   [SplDoublyLinkedList::getIteratorMode](spldoublylinkedlist.getiteratormode.html) — Повертає режим ітерації
-   [SplDoublyLinkedList::isEmpty](spldoublylinkedlist.isempty.html) — Перевіряє, чи двозв'язковий список є порожнім.
-   [SplDoublyLinkedList::key](spldoublylinkedlist.key.html) — Повертає індекс поточного сайту
-   [SplDoublyLinkedList::next](spldoublylinkedlist.next.html) — Переміщує ітератор до наступного елементу
-   [SplDoublyLinkedList::offsetExists](spldoublylinkedlist.offsetexists.html) — Перевіряє, чи існує запитуваний індекс
-   [SplDoublyLinkedList::offsetGet](spldoublylinkedlist.offsetget.html) — Повертає значення за вказаним індексом
-   [SplDoublyLinkedList::offsetSet](spldoublylinkedlist.offsetset.html) — Встановлює значення за заданим індексом $index у $value
-   [SplDoublyLinkedList::offsetUnset](spldoublylinkedlist.offsetunset.html) — Видаляє значення за вказаним індексом $index
-   [SplDoublyLinkedList::pop](spldoublylinkedlist.pop.html) - Видаляє (виштовхує) вузол, що знаходиться в кінці двозв'язкового списку
-   [SplDoublyLinkedList::prev](spldoublylinkedlist.prev.html) — Переміщує ітератор до попереднього елемента
-   [SplDoublyLinkedList::push](spldoublylinkedlist.push.html) — Поміщає елемент до кінця двозв'язкового списку
-   [SplDoublyLinkedList::rewind](spldoublylinkedlist.rewind.html) — Повертає ітератор на початок
-   [SplDoublyLinkedList::serialize](spldoublylinkedlist.serialize.html) — Серіалізує сховище
-   [SplDoublyLinkedList::setIteratorMode](spldoublylinkedlist.setiteratormode.html) - Встановлює режим ітерації
-   [SplDoublyLinkedList::shift](spldoublylinkedlist.shift.html) - Видаляє вузол, що знаходиться на початку двозв'язкового списку
-   [SplDoublyLinkedList::top](spldoublylinkedlist.top.html) — Отримує вузол, що знаходиться наприкінці двозв'язкового списку.
-   [SplDoublyLinkedList::unserialize](spldoublylinkedlist.unserialize.html) - Десеріалізує сховище
-   [SplDoublyLinkedList::unshift](spldoublylinkedlist.unshift.html) — Вставляє елемент на початок двозв'язкового списку
-   [SplDoublyLinkedList::valid](spldoublylinkedlist.valid.html) — Перевіряє, чи містить вузли двозв'язковий список