Повертає останнє значення двосторонньої черги

-   [« Ds\\Deque::jsonSerialize](ds-deque.jsonserialize.html)
    
-   [Ds\\Deque::map »](ds-deque.map.html)
    
-   [PHP Manual](index.html)
    
-   [Двухсторонняя очередь](class.ds-deque.html)
    
-   Повертає останнє значення двосторонньої черги
    

# ДсDeque::last

(PECL ds >= 1.0.0)

ДсDeque::last — Повертає останнє значення двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::last(): mixed
```

Повертає останнє значення двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент двосторонньої черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо двостороння черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::last()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```