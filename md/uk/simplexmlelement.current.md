---
navigation:
  - simplexmlelement.count.md: '« SimpleXMLElement::count'
  - simplexmlelement.getdocnamespaces.md: 'SimpleXMLElement::getDocNamespaces »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::current

(No version information available, might only be in Git)

SimpleXMLElement::current — Повертає поточний елемент

### Опис

```methodsynopsis
public SimpleXMLElement::current(): SimpleXMLElement
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::current()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод повертає поточний елемент як об'єкта [SimpleXMLElement](class.simplexmlelement.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний елемент як об'єкт [SimpleXMLElement](class.simplexmlelement.md)

### Помилки

Викидає [Error](class.error.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Якщо **SimpleXMLElement::current()** викликається на некоректному ітераторі, то тепер видається помилка [Error](class.error.md); раніше поверталося значення **`null`** |

### Приклади

**Приклад #1 Повернення поточного елемента**

```php
<?php
$xmlElement = new SimpleXMLElement('<books><book>PHP basics</book><book>XML basics</book></books>');
var_dump($xmlIElement->current());

$xmlElement->rewind(); // перемотка к первому элементу, иначе current() не будет работать
?>
```

Результат виконання наведеного прикладу:

```
object(SimpleXMLElement)#2 (1) {
  [0]=>
  string(10) "PHP basics"
}
```

### Дивіться також

-   [SimpleXMLElement::key()](simplexmlelement.key.md) \- Повертає ім'я XML-тегу поточного елемента
-   [SimpleXMLElement::next()](simplexmlelement.next.md) \- Перехід до наступного елементу
-   [SimpleXMLElement::rewind()](simplexmlelement.rewind.md) \- Перемотування до першого елементу
-   [SimpleXMLElement::valid()](simplexmlelement.valid.md) \- Перевіряє, чи є поточний елемент коректним
-   [SimpleXMLElement](class.simplexmlelement.md)
