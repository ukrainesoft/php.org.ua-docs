---
navigation:
  - class.regexiterator.html: « RegexIterator
  - regexiterator.construct.html: 'RegexIterator::construct »'
  - index.html: PHP Manual
  - class.regexiterator.html: RegexIterator
title: 'RegexIterator::accept'
---
# RegexIterator::accept

(PHP 5> = 5.2.0, PHP 7, PHP 8)

RegexIterator::accept — Перевірка відповідності регулярному виразу

### Опис

```methodsynopsis
public RegexIterator::accept(): bool
```

Перевіряє відповідність рядка `(string)`, яку повернув метод **RegexIterator::current()** (або **RegexIterator::key()**, якщо встановлено прапор [RegexIterator::USEKEY](class.regexiterator.html#regexiterator.constants.use-key)), регулярному виразу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо значення елемента відповідає регулярному виразу, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::accept()****

У цьому прикладі буде здійснюватись навігація тільки по тих елементах, значення яких відповідають регулярному виразу.

```php
<?php
$names = new ArrayIterator(array('Ann', 'Bob', 'Charlie', 'David'));
$filter = new RegexIterator($names, '/^[B-D]/');
foreach ($filter as $name) {
    echo $name . PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
Bob
Charlie
David
```

### Дивіться також

-   [Константи RegexIterator](class.regexiterator.html#regexiterator.constants)
-   [RegexIterator::setFlags()](regexiterator.setflags.html) - Установка прапорів
