- [« SimpleXMLIterator::next](simplexmliterator.next.md)
- [SimpleXMLIterator::valid »](simplexmliterator.valid.md)

- [PHP Manual](index.md)
- [SimpleXMLIterator](class.simplexmliterator.md)
- Повертає ітератор до першого елементу

# SimpleXMLIterator::rewind

(PHP 5, PHP 7, PHP 8)

SimpleXMLIterator::rewind — Повертає ітератор до першого елементу

### Опис

public **SimpleXMLIterator::rewind**(): void

Цей метод повертає [SimpleXMLIterator](class.simplexmliterator.md)
до першого елементу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Повернення до першого елемента**

` <?php$xmlIterator = new SimpleXMLIterator('<books><book>Основи PHP</book><book>Основи XML</book></books>');$xmlIterator->rewind();var_dump($ xmlIterator->current());?> `

Результат виконання цього прикладу:

object(SimpleXMLIterator)#2 (1) {
[0]=>
string(10) "Основи PHP"
}
