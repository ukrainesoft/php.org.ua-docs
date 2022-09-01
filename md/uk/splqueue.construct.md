---
navigation:
  - class.splqueue.html: « SplQueue
  - splqueue.dequeue.html: 'SplQueue::dequeue »'
  - index.html: PHP Manual
  - class.splqueue.html: SplQueue
title: 'SplQueue::construct'
---
# SplQueue::construct

(PHP 5> = 5.3.0, PHP 7)

SplQueue::construct - Створює нову чергу, реалізовану з використанням двозв'язкового списку

### Опис

public **SplQueue::construct**

Створює нову порожню чергу.

> **Зауваження**
> 
> Метод автоматично встановлює режим ітератора SplDoublyLinkedList::ITMODEFIFO.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **SplQueue::construct()****

```php
<?php
$q = new SplQueue();

$q[] = 1;
$q[] = 2;
$q[] = 3;

foreach ($q as $elem)  {
 echo $elem."\n";
}
?>
```

Результат виконання цього прикладу:

```
1
2
3
```

**Приклад #2 Ефективна обробка завдань за допомогою [SplQueue](class.splqueue.html)**

```php
<?php
$q = new SplQueue();
$q->setIteratorMode(SplQueue::IT_MODE_DELETE);

// ... поставить несколько задач в очередь ...

// обработать их
foreach ($q as $task) {
    // ... обработать $task ...

    // добавить новые задачи в очередь
    $q[] = $newTask;
    // ...
}
?>
```
