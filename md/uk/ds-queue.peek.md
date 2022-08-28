Повертає значення з початку черги

-   [« Ds\\Queue::jsonSerialize](ds-queue.jsonserialize.html)
    
-   [Ds\\Queue::pop »](ds-queue.pop.html)
    
-   [PHP Manual](index.html)
    
-   [Очередь](class.ds-queue.html)
    
-   Повертає значення з початку черги
    

# ДсQueue::peek

(PECL ds >= 1.0.0)

ДсQueue::peek — Повертає значення з початку черги

### Опис

```methodsynopsis
public Ds\Queue::peek(): mixed
```

Повертає значення із початку черги, але не видаляє його.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення із початку черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::peek()****

```php
<?php
$queue = new \Ds\Queue();

$queue->push("a");
$queue->push("b");
$queue->push("c");

var_dump($queue->peek());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
```