Створює новий екземпляр

-   [« DsQueue::clear](ds-queue.clear.html)
    
-   [ДсQueue::copy »](ds-queue.copy.html)
    
-   [PHP Manual](index.html)
    
-   [Черга](class.ds-queue.html)
    
-   Створює новий екземпляр
    

# ДсQueue::construct

(PECL ds >= 1.0.0)

ДсQueue::construct — Створює новий екземпляр

### Опис

public **ДсQueue::construct**[mixed](language.types.declarations.html#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.html), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсQueue::construct()****

```php
<?php
$queue = new \Ds\Queue();
var_dump($queue);


$queue = new \Ds\Queue([1, 2, 3]);
var_dump($queue);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Queue)#2 (0) {
}
object(Ds\Queue)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```