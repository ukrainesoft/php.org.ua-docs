---
navigation:
  - class.regexiterator.md: « RegexIterator
  - regexiterator.construct.md: 'RegexIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.regexiterator.md: RegexIterator
title: 'RegexIterator::accept'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RegexIterator::accept

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

RegexIterator::accept — Перевірка відповідності регулярному виразу

### Опис

```methodsynopsis
public RegexIterator::accept(): bool
```

Перевіряє відповідність рядка `(string)`, яку повернув метод **RegexIterator::current()**(или**RegexIterator::key()**, если установлен флаг[RegexIterator::USE\_KEY](class.regexiterator.md#regexiterator.constants.use-key)), регулярному виразу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

\*\*`true`\*\*якщо значення елемента відповідає регулярному виразу, **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**RegexIterator::accept()\*\*\*\*

У цьому прикладі буде здійснюватись навігація тільки по тих елементах, значення яких відповідають регулярному виразу.

```php
<?php
$names = new ArrayIterator(array('Ann', 'Bob', 'Charlie', 'David'));
$filter = new RegexIterator($names, '/^[B-D]/');
foreach ($filter as $name) {
    echo $name . PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
Bob
Charlie
David
```

### Дивіться також

-   [Константи RegexIterator](class.regexiterator.md#regexiterator.constants)
-   [RegexIterator::setFlags()](regexiterator.setflags.md) \- Установка прапорів
