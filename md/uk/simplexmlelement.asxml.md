Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML

-   [« SimpleXMLElement::addChild](simplexmlelement.addchild.html)
    
-   [SimpleXMLElement::attributes »](simplexmlelement.attributes.html)
    
-   [PHP Manual](index.html)
    
-   [SimpleXMLElement](class.simplexmlelement.html)
    
-   Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML
    

# SimpleXMLElement::asXML

(PHP 5, PHP 7, PHP 8)

SimpleXMLElement::asXML — Повертає сформований XML-документ у вигляді рядка на основі елемента SimpleXML

### Опис

```methodsynopsis
public SimpleXMLElement::asXML(?string $filename = null): string|bool
```

Метод `asXML` визначає формат даних батьківських об'єктів у версії XML 1.0.

### Список параметрів

`filename`

Якщо вказано значення у вигляді рядка (string), то функція запише дані у файл, а чи не поверне їх.

### Значення, що повертаються

Якщо `filename` не вказано, то функція поверне рядок (string) у разі успішного виконання та **`false`** у разі виникнення помилки. Якщо параметр вказано, то функція поверне **`true`**, якщо файл буде успішно записаний та **`false`** в іншому випадку.

### список змін

| Версия | Описание                                 |
|--------|------------------------------------------|
|        | `filename` тепер допускає значення null. |

### Приклади

**Приклад #1 Отримання XML**

```php
<?php
$string = <<<XML
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

$xml = new SimpleXMLElement($string);

echo $xml->asXML();

?>
```

Результат виконання цього прикладу:

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

**Приклад #2 Використання asXML() з результатами [SimpleXMLElement::xpath()](simplexmlelement.xpath.html)**

```php
<?php
// Продолжение примера XML выше.

/* Поиск <a><b><c> */
$result = $xml->xpath('/a/b/c');

foreach ($result as $node) {
    echo $node->asXML();
}
?>
```

Результат виконання цього прикладу:

```
<c>текст</c><c>штучка</c>
```

### Дивіться також

-   [SimpleXMLElement::toString()](simplexmlelement.tostring.html) - Повертає вміст рядка
-   [Базовое использование SimpleXML](simplexml.examples-basic.html)