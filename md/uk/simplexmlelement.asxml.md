---
navigation:
  - simplexmlelement.addchild.md: '« SimpleXMLElement::addChild'
  - simplexmlelement.attributes.md: 'SimpleXMLElement::attributes »'
  - index.md: PHP Manual
  - class.simplexmlelement.md: SimpleXMLElement
title: 'SimpleXMLElement::asXML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SimpleXMLElement::asXML

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::asXML — Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML

### Опис

```methodsynopsis
public SimpleXMLElement::asXML(?string $filename = null): string|bool
```

Метод`asXML` визначає формат даних батьківських об'єктів у версії XML 1.0.

### Список параметрів

`filename`

Якщо вказано значення у вигляді рядка (string), то функція запише дані у файл, а чи не поверне їх.

### Значення, що повертаються

Якщо `filename` не вказано, то функція поверне рядок (string) у разі успішного виконання та **`false`** у разі виникнення помилки. Якщо параметр вказано, то функція поверне **`true`**, якщо файл буде успішно записаний та **`false`** в іншому випадку.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `filename` тепер допускає значення null. |

### Приклади

**Приклад #1 Отримання XML**

```php
<?php
$string = <<<XML
<a>
 <b>
  <c>текст</c>
  <c>штучка</c>
 </b>
 <d>
  <c>код</c>
 </d>
</a>
XML;

$xml = new SimpleXMLElement($string);

echo $xml->asXML();

?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<a>
 <b>
  <c>текст</c>
  <c>штучка</c>
 </b>
 <d>
  <c>код</c>
 </d>
</a>
```

`asXML` також працює з результатами Xpath:

**Пример #2 Использование asXML() с результатами[SimpleXMLElement::xpath()](simplexmlelement.xpath.md)**

```php
<?php
// Продолжение примера XML выше.

/* Поиск <a><b><c> */
$result = $xml->xpath('/a/b/c');

foreach ($result as $node) {
    echo $node->asXML();
}
?>
```

Результат виконання наведеного прикладу:

```
<c>текст</c><c>штучка</c>
```

### Дивіться також

-   [SimpleXMLElement::\_\_toString()](simplexmlelement.tostring.md) \- Повертає вміст рядка
-   [Базове використання SimpleXML](simplexml.examples-basic.md)
