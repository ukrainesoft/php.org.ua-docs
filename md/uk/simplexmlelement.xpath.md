---
navigation:
  - simplexmlelement.valid.md: '« SimpleXMLElement::valid'
  - class.simplexmliterator.md: SimpleXMLIterator »
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::xpath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::xpath

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::xpath — Запускає запит XPath до XML-даних

### Опис

```methodsynopsis
public SimpleXMLElement::xpath(string $expression): array|null|false
```

Метод`xpath` шукає вузли SimpleXML з дочірніми елементами, що відповідають XPath `expression`

### Список параметрів

`expression`

Шлях XPath

### Значення, що повертаються

Повертає масив (array) об'єктів SimpleXMLElement у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Xpath**

```php
<?php
$string = <<<XML
<a>
 <b>
  <c>текст</c>
  <c>вещь</c>
 </b>
 <d>
  <c>код</c>
 </d>
</a>
XML;

$xml = new SimpleXMLElement($string);

/* Поиск <a><b><c> */
$result = $xml->xpath('/a/b/c');

foreach ($result as $node) {
    echo '/a/b/c: ',$node,"\n";
}

/* Относительные пути также работают... */
$result = $xml->xpath('b/c');

foreach ($result as $node) {
    echo 'b/c: ',$node,"\n";
}
?>
```

Результат виконання наведеного прикладу:

```
/a/b/c: текст
/a/b/c: вещь
b/c: текст
b/c: вещь
```

Зверніть увагу, що обидва результати однакові.

### Дивіться також

-   [SimpleXMLElement::registerXPathNamespace()](simplexmlelement.registerxpathnamespace.md) \- Створює префікс/простір імен контексту для наступного запиту XPath
-   [SimpleXMLElement::getDocNamespaces()](simplexmlelement.getdocnamespaces.md) \- Повертає простори імен, оголошених у документі
-   [SimpleXMLElement::getNamespaces()](simplexmlelement.getnamespaces.md) \- Повертає простір імен, які використовуються в документі
-   [Базове використання SimpleXML](simplexml.examples-basic.md)
