Запускає запит XPath до XML-даних

-   [« SimpleXMLElement::\_\_toString](simplexmlelement.tostring.html)
    
-   [SimpleXMLIterator »](class.simplexmliterator.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLElement](class.simplexmlelement.html)
    
-   Запускає запит XPath до XML-даних
    

# SimpleXMLElement::xpath

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::xpath — Запускає запит XPath до XML-даних

### Опис

```methodsynopsis
public SimpleXMLElement::xpath(string $expression): array|null|false
```

Метод `xpath` шукає вузли SimpleXML з дочірніми елементами, що відповідають XPath `expression`

### Список параметрів

`expression`

Шлях XPath

### Значення, що повертаються

Повертає масив (array) об'єктів SimpleXMLElement у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Xpath**

```php
<?php
$string = <<<XML
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

$xml = new SimpleXMLElement($string);

/* Поиск <a><b><c> */
$result = $xml->xpath('/a/b/c');

foreach ($result as $node) {
    echo '/a/b/c: ',$node,"\n";
}

/* Относительные пути также работают... */
$result = $xml->xpath('b/c');

foreach ($result as $node) {
    echo 'b/c: ',$node,"\n";
}
?>
```

Результат виконання цього прикладу:

```
/a/b/c: текст
/a/b/c: вещь
b/c: текст
b/c: вещь
```

Зверніть увагу, що обидва результати однакові.

### Дивіться також

-   [SimpleXMLElement::registerXPathNamespace()](simplexmlelement.registerxpathnamespace.html) - Створює префікс/простір імен контексту для наступного запиту XPath
-   [SimpleXMLElement::getDocNamespaces()](simplexmlelement.getdocnamespaces.html) - Повертає простори імен, оголошених у документі
-   [SimpleXMLElement::getNamespaces()](simplexmlelement.getnamespaces.html) - Повертає простір імен, що використовуються в документі
-   [Базовое использование SimpleXML](simplexml.examples-basic.html)