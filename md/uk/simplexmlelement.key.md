---
navigation:
  - simplexmlelement.haschildren.md: '« SimpleXMLElement::hasChildren'
  - simplexmlelement.next.md: 'SimpleXMLElement::next »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::key

(No version information available, might only be in Git)

SimpleXMLElement::key — Повертає ім'я XML-тегу поточного елемента

### Опис

```methodsynopsis
public SimpleXMLElement::key(): string
```

**Увага**

До версії PHP 8.0 метод **SimpleXMLElement::key()** був оголошений лише для дочірнього класу [SimpleXMLIterator](class.simplexmliterator.md)

Метод одержує ім'я XML-тега поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я XML-тегу елемента, на який посилається поточний об'єкт [SimpleXMLElement](class.simplexmlelement.md)

### Помилки

Викидає [Error](class.error.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | У разі виклику методу **SimpleXMLElement::key()** на некоректному ітераторі тепер видається помилка [Error](class.error.md); раніше поверталося значення **`false`** |

### Приклади

**Приклад #1 Отримання поточного ключа тега XML**

```php
<?php
$xmlElement = new SimpleXMLElement('<books><book>PHP basics</book><book>XML basics</book></books>');

echo var_dump($xmlElement->key());
$xmlElement->rewind(); // перемотка к первому элементу
echo var_dump($xmlElement->key());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
string(4) "book"
```
