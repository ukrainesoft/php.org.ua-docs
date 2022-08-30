Перевіряє коректність поточної позиції

-   [« Iterator::rewind](iterator.rewind.md)
    
-   [IteratorAggregate »](class.iteratoraggregate.md)
    
-   [PHP Manual](index.md)
    
-   [Iterator](class.iterator.md)
    
-   Перевіряє коректність поточної позиції
    

# Iterator::valid

(PHP 5, PHP 7, PHP 8)

Iterator::valid — Перевіряє коректність поточної позиції

### Опис

```methodsynopsis
public Iterator::valid(): bool
```

Метод викликається після функцій [Iterator::rewind()](iterator.rewind.md) і [Iterator::next()](iterator.next.md) щоб перевірити, чи припустима поточна позиція.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення, що повертається, буде приведено до логічного типу (bool) і потім використано. Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.