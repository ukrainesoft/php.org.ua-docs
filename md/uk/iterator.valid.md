Перевіряє коректність поточної позиції

-   [« Iterator::rewind](iterator.rewind.html)
    
-   [IteratorAggregate »](class.iteratoraggregate.html)
    
-   [PHP Manual](index.html)
    
-   [Iterator](class.iterator.html)
    
-   Перевіряє коректність поточної позиції
    

# Iterator::valid

(PHP 5, PHP 7, PHP 8)

Iterator::valid — Перевіряє коректність поточної позиції

### Опис

```methodsynopsis
public Iterator::valid(): bool
```

Метод викликається після функцій [Iterator::rewind()](iterator.rewind.html) і [Iterator::next()](iterator.next.html) щоб перевірити, чи припустима поточна позиція.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення, що повертається, буде приведено до логічного типу (bool) і потім використано. Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.