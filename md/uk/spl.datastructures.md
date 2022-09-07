---
navigation:
  - spl.constants.md: « Обумовлені константи
  - class.spldoublylinkedlist.md: SplDoublyLinkedList »
  - index.md: PHP Manual
  - book.spl.md: SPL
title: Структури даних
---
# Структури даних

## Зміст

-   [SplDoublyLinkedList](class.spldoublylinkedlist.md)
-   [SplStack](class.splstack.md)
-   [SplQueue](class.splqueue.md)
-   [SplHeap](class.splheap.md)
-   [SplMaxHeap](class.splmaxheap.md)
-   [SplMinHeap](class.splminheap.md)
-   [SplPriorityQueue](class.splpriorityqueue.md)
-   [SplFixedArray](class.splfixedarray.md)
-   [SplObjectStorage](class.splobjectstorage.md)

SPL надає набір стандартних структур даних. Вони згруповані тут за своєю базовою реалізацією, яка зазвичай визначає їх загальну сферу застосування.

## Двозв'язкові списки

Двозв'язковий список (DLL) – це список вузлів, пов'язаних в обох напрямках один з одним. Операції ітератора, доступ до обох кінців, додавання або видалення вузлів вартістю O(1), коли основною структурою є DLL. Отже, вони забезпечує хорошу реалізацію для стеків та черг.

-   [SplDoublyLinkedList](class.spldoublylinkedlist.md)
    -   [SplStack](class.splstack.md)
    -   [SplQueue](class.splqueue.md)

## Купи

Купи - це деревоподібні структури, які випливають властивостями купи: кожен вузол більше або дорівнює своїм нащадкам, при цьому для порівняння використовується впроваджений метод порівняння, який є загальним для всієї купи.

-   [SplHeap](class.splheap.md)
    -   [SplMaxHeap](class.splmaxheap.md)
    -   [SplMinHeap](class.splminheap.md)
-   [SplPriorityQueue](class.splpriorityqueue.md)

## Масиви

Масиви - структури, які зберігають дані у безперервному вигляді, доступні через індекси. Не плутайте їх із масивами PHP: останні насправді реалізовані у вигляді впорядкованих хеш-таблиць.

-   [SplFixedArray](class.splfixedarray.md)

## Мапа

Карта – це структура даних, що містить пари ключ-значення. Масиви PHP можна розглядати як карти, що відображають цілі/рядкові дані в їх значення. SPL надає карту, яка відображає об'єкти до даних. Ця карта також може бути використана як багато об'єктів.

-   [SplObjectStorage](class.splobjectstorage.md)
