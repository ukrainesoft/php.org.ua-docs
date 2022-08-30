Повертає перший елемент двосторонньої черги

-   [« DsDeque::find](ds-deque.find.html)
    
-   [ДсDeque::get »](ds-deque.get.html)
    
-   [PHP Manual](index.html)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Повертає перший елемент двосторонньої черги
    

# ДсDeque::first

(PECL ds >= 1.0.0)

ДсDeque::first — Повертає перший елемент двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::first(): mixed
```

Повертає перший елемент двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент двосторонньої черги.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо двостороння черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::first()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```