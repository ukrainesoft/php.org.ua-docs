---
navigation:
  - simplexmlelement.addattribute.md: '« SimpleXMLElement::addAttribute'
  - simplexmlelement.asxml.md: 'SimpleXMLElement::asXML »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::addChild'
---
# SimpleXMLElement::addChild

(PHP 5> = 5.1.3, PHP 7, PHP 8)

SimpleXMLElement::addChild — Додає дочірній елемент до сайту XML

### Опис

```methodsynopsis
public SimpleXMLElement::addChild(string $qualifiedName, ?string $value = null, ?string $namespace = null): ?SimpleXMLElement
```

Додає дочірній елемент до вузла та повертає нащадка SimpleXMLElement.

### Список параметрів

`qualifiedName`

Ім'я дочірнього елемента, що додається.

`value`

Якщо вказано, значення (вміст) дочірнього елемента.

`namespace`

Якщо зазначено, то простір імен, якого належить дочірній елемент.

### Значення, що повертаються

Метод `addChild` повертає об'єкт [SimpleXMLElement](class.simplexmlelement.md), Що представляє доданого нащадка до вузла XML у разі успішного виконання; **`null`** у разі виникнення помилки.

### Приклади

> **Зауваження**
> 
> Перелічені приклади можуть містити `example.php`, в якому визначається XML-рядок, розташована в першому прикладі посібника з [базовому использованию](simplexml.examples-basic.md)

**Приклад #1 Додавання атрибутів та нащадків до елемента SimpleXML**

```php
<?php

include 'example.php';

$sxe = new SimpleXMLElement($xmlstr);
$sxe->addAttribute('type', 'documentary');

$movie = $sxe->addChild('movie');
$movie->addChild('title', 'PHP2: Истории парсера');
$movie->addChild('plot', 'Все о людях, создававших его.');

$characters = $movie->addChild('characters');
$character  = $characters->addChild('character');
$character->addChild('name', 'Mr. Parser');
$character->addChild('actor', 'John Doe');

$rating = $movie->addChild('rating', '5');
$rating->addAttribute('type', 'stars');

echo $sxe->asXML();

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
<?xml version="1.0" standalone="yes"?>
<movies type="documentary">
 <movie>
  <title>PHP: Появление Парсера</title>
  <characters>
   <character>
    <name>Ms. Coder</name>
    <actor>Onlivia Actora</actor>
   </character>
   <character>
    <name>Mr. Coder</name>
    <actor>El Act&#xD3;r</actor>
   </character>
  </characters>
  <plot>
   Таким образом, это язык. Это всё равно язык программирования. Или
   это скриптовый язык? Все раскрывается в этом документальном фильме,
   похожем на фильм ужасов.
  </plot>
  <great-lines>
   <line>PHP решает все мои задачи в web</line>
  </great-lines>
  <rating type="thumbs">7</rating>
  <rating type="stars">5</rating>
 </movie>
 <movie>
  <title>PHP2: Истории парсера</title>
  <plot>Все о людях, создававших его.</plot>
  <characters>
   <character>
    <name>Mr. Parser</name>
    <actor>John Doe</actor>
   </character>
  </characters>
  <rating type="stars">5</rating>
 </movie>
</movies>
```

### Дивіться також

-   [SimpleXMLElement::addAttribute()](simplexmlelement.addattribute.md) - Додає атрибут до SimpleXML-елементу
-   [Базовое использование SimpleXML](simplexml.examples-basic.md)
