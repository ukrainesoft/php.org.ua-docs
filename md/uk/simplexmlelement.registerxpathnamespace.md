---
navigation:
  - simplexmlelement.getnamespaces.md: '« SimpleXMLElement::getNamespaces'
  - simplexmlelement.savexml.md: 'SimpleXMLElement::saveXML »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::registerXPathNamespace'
---
# SimpleXMLElement::registerXPathNamespace

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SimpleXMLElement::registerXPathNamespace — Створює префікс/простір імен контексту для наступного запиту XPath

### Опис

```methodsynopsis
public SimpleXMLElement::registerXPathNamespace(string $prefix, string $namespace): bool
```

Створює префікс/простір імен контексту для наступного запиту XPath. Зокрема це необхідно, якщо постачальник цього XML-документа змінює префікс простору імен . `registerXPathNamespace` створить префікс для пов'язаного простору імен, дозволяючи отримати доступ до вузлів у цьому просторі імен без необхідності зміни коду, що враховує нові префікси, надані постачальником.

### Список параметрів

`prefix`

Префікс використовуваного простору імен у запиті XPath для отримання простору імен `namespace`

`namespace`

Використовуваний простір імен для запиту XPath. Воно має відповідати простору імен у XML-документі або запит XPath, що використовує `prefix` не дасть жодних результатів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення префіксу простору імен для використання у запиті XPath**

```php
<?php

$xml = <<<EOD
<book xmlns:chap="http://example.org/chapter-title">
    <title>My Book</title>
    <chapter id="1">
        <chap:title>Chapter 1</chap:title>
        <para>Donec velit. Nullam eget tellus vitae tortor gravida scelerisque.
            In orci lorem, cursus imperdiet, ultricies non, hendrerit et, orci.
            Nulla facilisi. Nullam velit nisl, laoreet id, condimentum ut,
            ultricies id, mauris.</para>
    </chapter>
    <chapter id="2">
        <chap:title>Chapter 2</chap:title>
        <para>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Proin
            gravida. Phasellus tincidunt massa vel urna. Proin adipiscing quam
            vitae odio. Sed dictum. Ut tincidunt lorem ac lorem. Duis eros
            tellus, pharetra id, faucibus eu, dapibus dictum, odio.</para>
    </chapter>
</book>
EOD;

$sxe = new SimpleXMLElement($xml);

$sxe->registerXPathNamespace('c', 'http://example.org/chapter-title');
$result = $sxe->xpath('//c:title');

foreach ($result as $title) {
  echo $title . "\n";
}

?>
```

Результат виконання цього прикладу:

```
Chapter 1
Chapter 2
```

Зверніть увагу на те, як у прикладі XML-документу встановлюється простір імен з префіксом `chap`. Уявіть, що цей документ (або інший схожий) використав префікс `c` у минулому для того самого простору імен. Так як він змінився, запит XPath більше не поверне правильних результатів і запит доведеться змінювати. Використання `registerXPathNamespace` дозволяє уникнути майбутніх модифікацій запитів, навіть якщо постачальник змінить префікс простору імен.

### Дивіться також

-   [SimpleXMLElement::xpath()](simplexmlelement.xpath.md) - Запускає запит XPath до XML-даних
-   [SimpleXMLElement::getDocNamespaces()](simplexmlelement.getdocnamespaces.md) - Повертає простори імен, оголошених у документі
-   [SimpleXMLElement::getNamespaces()](simplexmlelement.getnamespaces.md) - Повертає простір імен, що використовуються в документі
