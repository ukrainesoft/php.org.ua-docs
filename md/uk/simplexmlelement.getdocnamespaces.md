---
navigation:
  - simplexmlelement.count.md: '« SimpleXMLElement::count'
  - simplexmlelement.getname.md: 'SimpleXMLElement::getName »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::getDocNamespaces'
---
# SimpleXMLElement::getDocNamespaces

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SimpleXMLElement::getDocNamespaces — Повертає простір імен, оголошених у документі

### Опис

```methodsynopsis
public SimpleXMLElement::getDocNamespaces(bool $recursive = false, bool $fromRoot = true): array|false
```

Повертає простір імен, оголошених у документі

### Список параметрів

`recursive`

Якщо зазначено, то повертає всі оголошені простори імен у батьківського вузла та його дочірніх елементів. Інакше повертає лише оголошений простір імен кореневого вузла.

`fromRoot`

Дозволяє рекурсивно перевірити простір імен біля дочірнього вузла замість кореневого вузла XML документа.

### Значення, що повертаються

Метод `getDocNamespaces` повертає масив (array) з назвами просторів імен та пов'язаними з ними URI.

### Приклади

**Приклад #1 Отримання простору імен документа**

```php
<?php

$xml = <<<XML
<?xml version="1.0" standalone="yes"?>
<people xmlns:p="http://example.org/ns">
    <p:person id="1">John Doe</p:person>
    <p:person id="2">Susie Q. Public</p:person>
</people>
XML;

$sxe = new SimpleXMLElement($xml);

$namespaces = $sxe->getDocNamespaces();
var_dump($namespaces);

?>
```

Результат виконання цього прикладу:

```
array(1) {
   ["p"]=>
   string(21) "http://example.org/ns"
}
```

**Приклад #2 Робота з кількома просторами імен**

```php
<?php

$xml = <<<XML
<?xml version="1.0" standalone="yes"?>
<people xmlns:p="http://example.org/ns" xmlns:t="http://example.org/test">
    <p:person t:id="1">John Doe</p:person>
    <p:person t:id="2" a:addr="123 Street" xmlns:a="http://example.org/addr">
        Susie Q. Public
    </p:person>
</people>
XML;

$sxe = new SimpleXMLElement($xml);

$namespaces = $sxe->getDocNamespaces(TRUE);
var_dump($namespaces);

?>
```

Результат виконання цього прикладу:

```
array(3) {
  ["p"]=>
  string(21) "http://example.org/ns"
  ["t"]=>
  string(23) "http://example.org/test"
  ["a"]=>
  string(23) "http://example.org/addr"
}
```

### Дивіться також

-   [SimpleXMLElement::getNamespaces()](simplexmlelement.getnamespaces.md) - Повертає простір імен, що використовуються в документі
-   [SimpleXMLElement::registerXPathNamespace()](simplexmlelement.registerxpathnamespace.md) - Створює префікс/простір імен контексту для наступного запиту XPath
