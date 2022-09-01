---
navigation:
  - class.simplexmlelement.md: « SimpleXMLElement
  - simplexmlelement.addchild.md: 'SimpleXMLElement::addChild »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::addAttribute'
---
# SimpleXMLElement::addAttribute

(PHP 5> = 5.1.3, PHP 7, PHP 8)

SimpleXMLElement::addAttribute — Додає атрибут до SimpleXML-елементу

### Опис

```methodsynopsis
public SimpleXMLElement::addAttribute(string $qualifiedName, string $value, ?string $namespace = null): void
```

Додає атрибут до SimpleXML-елементу.

### Список параметрів

`qualifiedName`

Назва атрибуту, що додається.

`value`

Значення атрибуту.

`namespace`

Необов'язковий параметр вказує на простір імен, до якого належить атрибут.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

> **Зауваження**
> 
> Перелічені приклади можуть містити `example.php`, в якому визначається XML-рядок, розташована в першому прикладі посібника з [базовому использованию](simplexml.examples-basic.md)

**Приклад #1 Додавання атрибутів та нащадків до SimpleXML-елементу**

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
   Итак, этот язык. Типа, язык программирования. Или
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

-   [SimpleXMLElement::addChild()](simplexmlelement.addchild.md) - Додає дочірній елемент до сайту XML
-   [Базовое использование SimpleXML](simplexml.examples-basic.md)
