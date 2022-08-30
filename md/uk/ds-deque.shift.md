Видаляє та повертає перше значення

-   [« DsDeque::set](ds-deque.set.html)
    
-   [ДсDeque::slice »](ds-deque.slice.html)
    
-   [PHP Manual](index.md)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Видаляє та повертає перше значення
    

# ДсDeque::shift

(PECL ds >= 1.0.0)

ДсDeque::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
public Ds\Deque::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо двостороння черга порожня.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::shift()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->shift());
var_dump($deque->shift());
var_dump($deque->shift());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```