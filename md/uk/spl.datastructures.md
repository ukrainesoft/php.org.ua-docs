Структури даних

-   [« Предопределённые константы](spl.constants.html)
    
-   [SplDoublyLinkedList »](class.spldoublylinkedlist.html)
    
-   [PHP Manual](index.html)
    
-   [SPL](book.spl.html)
    
-   Структури даних
    

# Структури даних

## Зміст

-   [SplDoublyLinkedList](class.spldoublylinkedlist.html)
-   [SplStack](class.splstack.html)
-   [SplQueue](class.splqueue.html)
-   [SplHeap](class.splheap.html)
-   [SplMaxHeap](class.splmaxheap.html)
-   [SplMinHeap](class.splminheap.html)
-   [SplPriorityQueue](class.splpriorityqueue.html)
-   [SplFixedArray](class.splfixedarray.html)
-   [SplObjectStorage](class.splobjectstorage.html)

SPL надає набір стандартних структур даних. Вони згруповані тут за своєю базовою реалізацією, яка зазвичай визначає їх загальну сферу застосування.

## Двозв'язкові списки

Двозв'язковий список (DLL) – це список вузлів, пов'язаних в обох напрямках один з одним. Операції ітератора, доступ до обох кінців, додавання або видалення вузлів вартістю O(1), коли основною структурою є DLL. Отже, вони забезпечує хорошу реалізацію для стеків та черг.

-   [SplDoublyLinkedList](class.spldoublylinkedlist.html)
    -   [SplStack](class.splstack.html)
    -   [SplQueue](class.splqueue.html)

## Купи

Купи - це деревоподібні структури, які випливають властивостями купи: кожен вузол більше або дорівнює своїм нащадкам, при цьому для порівняння використовується впроваджений метод порівняння, який є загальним для всієї купи.

-   [SplHeap](class.splheap.html)
    -   [SplMaxHeap](class.splmaxheap.html)
    -   [SplMinHeap](class.splminheap.html)
-   [SplPriorityQueue](class.splpriorityqueue.html)

## Масиви

Масиви - структури, які зберігають дані у безперервному вигляді, доступні через індекси. Не плутайте їх із масивами PHP: останні насправді реалізовані у вигляді впорядкованих хеш-таблиць.

-   [SplFixedArray](class.splfixedarray.html)

## Мапа

Карта – це структура даних, що містить пари ключ-значення. Масиви PHP можна розглядати як карти, що відображають цілі/рядкові дані в їх значення. SPL надає карту, яка відображає об'єкти до даних. Ця карта також може бути використана як багато об'єктів.

-   [SplObjectStorage](class.splobjectstorage.html)