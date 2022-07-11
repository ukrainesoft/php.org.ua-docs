- [« RecursiveRegexIterator::\_\_construct](recursiveregexiterator.construct.md)
- [RecursiveRegexIterator::hasChildren »](recursiveregexiterator.haschildren.md)

- [PHP Manual](index.md)
- [RecursiveRegexIterator](class.recursiveregexiterator.md)
- Повертає ітератор до поточного елемента

# RecursiveRegexIterator::getChildren

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

RecursiveRegexIterator::getChildren — Повертає ітератор для поточного
елемента

### Опис

public **RecursiveRegexIterator::getChildren**():
[RecursiveRegexIterator](class.recursiveregexiterator.md)

Повертає ітератор до поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ітератор для поточного елемента, якщо можлива навігація вмісту
внутрішнього ітератора.

### Помилки

Якщо внутрішній ітератор вказує на елемент, який не містить
дочірніх елементів, буде викинуто виняток
[InvalidArgumentException](class.invalidargumentexception.md).

### Приклади

**Приклад #1 Приклад використання
**RecursiveRegexIterator::getChildren()****

` <?php$rArrayIterator = new RecursiveArrayIterator(array('test1', array('tet3', 'test4', 'test5')));$rRegexIterator = new RecursiveRegexItera   ::ALL_MATCHES);foreach ($rRegexIterator as $key1 => $value1) {    if ($rRegexIterator->hasChildren()) {        // выведем все дочерние элементы        echo "Дочерние элементы: "; foreach ($rRegexIterator->getChildren() as $key => $value) {            echo $value . " "; }        echo "
";    }}else {        echo "Немає|дочірніх елементів
";    }}?> `

Результат виконання цього прикладу:

Немає дочірніх елементів
Дочірні елементи: test4 test5

### Дивіться також

- [RecursiveRegexIterator::hasChildren()](recursiveregexiterator.haschildren.md) -
Визначає, чи можлива навігація вмісту поточного елемента
