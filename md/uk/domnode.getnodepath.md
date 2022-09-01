---
navigation:
  - domnode.getlineno.md: '« DOMNode::getLineNo'
  - domnode.hasattributes.md: 'DOMNode::hasAttributes »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::getNodePath'
---
# DOMNode::getNodePath

(PHP 5> = 5.2.0, PHP 7, PHP 8)

DOMNode::getNodePath — Отримання XPath вузла

### Опис

```methodsynopsis
public DOMNode::getNodePath(): ?string
```

Отримує шлях XPath, яким розташований вузол.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що містить XPath або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **DOMNode::getNodePath()****

```php
<?php
// Создание объекта DOMDocument
$dom = new DOMDocument;

// Загрузка XML
$dom->loadXML('
<fruits>
 <apples>
  <apple>braeburn</apple>
  <apple>granny smith</apple>
 </apples>
 <pears>
  <pear>conference</pear>
 </pears>
</fruits>
');

// Вывод XPath для каждого элемента
foreach ($dom->getElementsByTagName('*') as $node) {
    echo $node->getNodePath() . "\n";
}
?>
```

Результат виконання цього прикладу:

```
/fruits
/fruits/apples
/fruits/apples/apple[1]
/fruits/apples/apple[2]
/fruits/pears
/fruits/pears/pear
```

### Дивіться також

-   [DOMXPath](class.domxpath.md)
