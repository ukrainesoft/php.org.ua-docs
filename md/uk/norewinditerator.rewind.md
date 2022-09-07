---
navigation:
  - norewinditerator.next.md: '« NoRewindIterator::next'
  - norewinditerator.valid.md: 'NoRewindIterator::valid »'
  - index.md: PHP Manual
  - class.norewinditerator.md: NoRewindIterator
title: 'NoRewindIterator::rewind'
---
# NoRewindIterator::rewind

(PHP 5> = 5.1.0, PHP 7, PHP 8)

NoRewindIterator::rewind — Запобігає поверненню внутрішнього ітератора на початок

### Опис

```methodsynopsis
public NoRewindIterator::rewind(): void
```

Запобігає поверненню внутрішнього ітератора на початок.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **NoRewindIterator::rewind()****

Приклад показує, що виклик операції повернення на початок об'єкта NoRewindIterator не має жодного ефекту.

```php
<?php
$fruits = array("лимон", "апельсин", "яблоко", "груша");

$noRewindIterator = new NoRewindIterator(new ArrayIterator($fruits));

echo $noRewindIterator->current() . "\n";
$noRewindIterator->next();
// возврат итератора в начало (ничего не должно случиться)
$noRewindIterator->rewind();
echo $noRewindIterator->current() . "\n";
?>
```

Результат виконання цього прикладу:

```
лимон
апельсин
```
