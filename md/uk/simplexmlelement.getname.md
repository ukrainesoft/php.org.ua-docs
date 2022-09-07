---
navigation:
  - simplexmlelement.getdocnamespaces.md: '« SimpleXMLElement::getDocNamespaces'
  - simplexmlelement.getnamespaces.md: 'SimpleXMLElement::getNamespaces »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::getName'
---
# SimpleXMLElement::getName

(PHP 5> = 5.1.3, PHP 7, PHP 8)

SimpleXMLElement::getName — Отримує ім'я елемента XML

### Опис

```methodsynopsis
public SimpleXMLElement::getName(): string
```

Отримує ім'я елемента XML.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод `getName` повертає ім'я XML тега у вигляді рядка (string), на який посилається об'єкт SimpleXMLElement.

### Приклади

> **Зауваження**
> 
> Перелічені приклади можуть містити `example.php`, в якому визначається XML-рядок, розташована в першому прикладі посібника з [базовому использованию](simplexml.examples-basic.md)

**Приклад #1 Отримання імен XML-елемента**

```php
<?php
include 'example.php';
$sxe = new SimpleXMLElement($xmlstr);

echo $sxe->getName() . "\n";

foreach ($sxe->children() as $child)
{
    echo $child->getName() . "\n";
}

?>
```

Результат виконання цього прикладу:

```
movies
movie
```
