---
navigation:
  - class.splstack.md: « SplStack
  - splstack.setiteratormode.md: 'SplStack::setIteratorMode »'
  - index.md: PHP Manual
  - class.splstack.md: SplStack
title: 'SplStack::construct'
---
# SplStack::construct

(PHP 5> = 5.3.0, PHP 7)

SplStack::construct — Створює новий стек, реалізований за допомогою двозв'язкового списку

### Опис

public **SplStack::construct**

Створює новий пустий стек.

> **Зауваження**
> 
> Метод автоматично встановлює режим ітератора SplDoublyLinkedList::ITMODELIFO.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання **SplStack::construct()****

```php
<?php
$q = new SplStack();

$q[] = 1;
$q[] = 2;
$q[] = 3;

foreach ($q as $elem)  {
 echo $elem."\n";
}
?>
```

Результат виконання цього прикладу:

```
3
2
1
```
