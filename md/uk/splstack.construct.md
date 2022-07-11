- [«SplStack](class.splstack.md)
- [SplStack::setIteratorMode »](splstack.setiteratormode.md)

- [PHP Manual](index.md)
- [SplStack](class.splstack.md)
- створює новий стек, реалізований з використанням двозв'язкового
списку

# SplStack::\_\_construct

(PHP 5 = 5.3.0, PHP 7)

SplStack::\_\_construct — Створює новий стек, реалізований з
використанням двозв'язкового списку

### Опис

public **SplStack::\_\_construct**()

Створює новий пустий стек.

> **Примітка**:
>
> Метод автоматично встановлює режим ітератора
> SplDoublyLinkedList::IT_MODE_LIFO.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **SplStack::\_\_construct()****

` <?php$q = new SplStack();$q[] = 1;$q[] = 2;$q[] = 3;foreach ($q as $elem)  { echo $elem."
";}?> `

Результат виконання цього прикладу:

3
2
1
