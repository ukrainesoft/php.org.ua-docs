---
navigation:
  - function.iterator-apply.md: « iterator\_apply
  - function.iterator-to-array.md: iterator\_to\_array »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: iterator\_count
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iterator\_count

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

iterator\_count — Підраховує кількість елементів в ітераторі

### Опис

```methodsynopsis
iterator_count(Traversable|array $iterator): int
```

Підраховує кількість елементів в ітераторі . **iterator\_count()** не гарантує збереження поточної позиції `iterator`

### Список параметрів

`iterator`

Ітератор, у якому провадиться підрахунок.

### Значення, що повертаються

Кількість елементів в ітераторі (`iterator`

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип параметра `iterator` був розширений з [Traversable](class.traversable.md)до[Traversable](class.traversable.md) |

### Приклади

**Пример #1 Пример использования**iterator\_count()\*\*\*\*

```php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_count($iterator));
?>
```

Результат виконання наведеного прикладу:

```
int(4)
```

**Пример #2**iterator\_count()\*\* модифікує позицію\*\*

```php
<?php
$iterator = new ArrayIterator(['one', 'two', 'three']);
var_dump($iterator->current());
var_dump(iterator_count($iterator));
var_dump($iterator->current());
?>
```

Результат виконання наведеного прикладу:

```
string(3) "one"
int(3)
NULL
```

**Пример #3**iterator\_count()\*\* у циклі [foreach](control-structures.foreach.md)\*\*

```php
<?php
$iterator = new ArrayIterator(['one', 'two', 'three']);
foreach ($iterator as $key => $value) {
    echo "$key: $value (", iterator_count($iterator), ")\n";
}?>
```

Результат виконання наведеного прикладу:

```
0: one (3)
```
