Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик

-   [« CallbackFilterIterator](class.callbackfilteriterator.md)
    
-   [CallbackFilterIterator::construct »](callbackfilteriterator.construct.md)
    
-   [PHP Manual](index.md)
    
-   [CallbackFilterIterator](class.callbackfilteriterator.md)
    
-   Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик
    

# CallbackFilterIterator::accept

(PHP 5> = 5.4.0, PHP 7, PHP 8)

CallbackFilterIterator::accept — Викликає callback-функцію і передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик

### Опис

```methodsynopsis
public CallbackFilterIterator::accept(): bool
```

Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик.

Callback-функція має повертати **`true`**, якщо поточний елемент пройшов фільтр, **`false`** в іншому випадку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо поточний елемент пройшов фільтр, **`false`** в іншому випадку.

### Дивіться також

-   [Приклади використання CallbackFilterIterator](class.callbackfilteriterator.html#callbackfilteriterator.examples)
-   [CallbackFilterIterator::construct()](callbackfilteriterator.construct.md) - Створює фільтруючий ітератор на основі іншого ітератора