- [« RegexIterator::\_\_construct](regexiterator.construct.md)
- [RegexIterator::getMode »](regexiterator.getmode.md)

- [PHP Manual](index.md)
- [RegexIterator](class.regexiterator.md)
- Отримання прапорів налаштування

# RegexIterator::getFlags

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

RegexIterator::getFlags — Отримання прапорців налаштування

### Опис

public **RegexIterator::getFlags**(): int

Повертає прапори настроювання. Список можливих прапорів наведено в описі
методу [RegexIterator::setFlags()](regexiterator.setflags.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає набір прапорів.

### Приклади

**Приклад #1 Приклад використання **RegexIterator::getFlags()****

` <?php$test = array ('str1' => 'test 1', 'teststr2' => 'another test', 'str3' => 'test 123');$arrayIterator = new Ar $regexIterator= new RegexIterator($arrayIterator, '/^test/');$regexIterator->setFlags(RegexIterator::USE_KEY);if ($regexIterator->getFlags() На: ключів масиву.';} else {    echo 'Фільтрація на основі значень масиву.';}?> `

Результат виконання цього прикладу:

Фільтрування на основі ключів масиву.

### Дивіться також

- [RegexIterator::setFlags()](regexiterator.setflags.md) - Установка
прапорів
