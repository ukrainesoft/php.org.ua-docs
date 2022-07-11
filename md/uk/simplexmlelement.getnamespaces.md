- [« SimpleXMLElement::getName](simplexmlelement.getname.md)
- [SimpleXMLElement::registerXPathNamespace »](simplexmlelement.registerxpathnamespace.md)

- [PHP Manual](index.md)
- [SimpleXMLElement](class.simplexmlelement.md)
- Повертає простір імен, що використовуються в документі

# SimpleXMLElement::getNamespaces

(PHP 5 \>= 5.1.2, PHP 7, PHP 8)

SimpleXMLElement::getNamespaces — Повертає простір імен,
використовуються в документі

### Опис

public **SimpleXMLElement::getNamespaces**(bool `$recursive` =
**`false`**): array

Повертає простір імен, що використовуються в документі

### Список параметрів

`recursive`
Якщо зазначено, то повертає всі використовувані простори імен
батьківського вузла та його дочірніх елементів. В іншому випадку
повертає використовується простір імен кореневого вузла.

### Значення, що повертаються

Метод `getNamespaces` повертає масив (array) із назвами просторів
імен та пов'язаними з ними URI.

### Приклади

**Приклад #1 Отримання просторів імен, які використовуються в документі**

` <?php$xml = <<<XML<?xml version="1.0" standalone="yes"?><people xmlns:p="http://example.org/ns" xmlns:t="http: //example.org/test">    <p:person id="1">John Doe</p:person>    <p:person id="2">Susie Q. Public</p:person></people >XML;$sxe = new SimpleXMLElement($xml);$namespaces = $sxe->getNamespaces(true);var_dump($namespaces);?> `

Результат виконання цього прикладу:

array(1) {
["p"]=>
string(21) "http://example.org/ns"
}

### Дивіться також

- [SimpleXMLElement::getDocNamespaces()](simplexmlelement.getdocnamespaces.md) -
Повертає простір імен, оголошених у документі
- [SimpleXMLElement::registerXPathNamespace()](simplexmlelement.registerxpathnamespace.md) -
Створює префікс/простір імен контексту для наступного запиту
XPath
