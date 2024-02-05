---
navigation:
  - domdocument.validate.md: '« DOMDocument::validate'
  - class.domdocumentfragment.md: DOMDocumentFragment »
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::xinclude'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::xinclude

(PHP 5, PHP 7, PHP 8)

DOMDocument::xinclude — Вставляє XInclude в об'єкті DOMDocument.

### Опис

```methodsynopsis
public DOMDocument::xinclude(int $options = 0): int|false
```

Цей метод вставляє [» блоки XInclude](http://www.w3.org/TR/xinclude/) в об'єкті класу DOMDocument.

> **Зауваження** :
> 
> Через те, що libxml2 автоматично дозволяє сутності, виклик цього методу призведе до несподіваних результатів у випадку, коли файл XML містить прикріплену схему DTD.

### Список параметрів

`options`

[Побітове АБО (`OR`) .](language.operators.bitwise.md) [констант опцій libxml](libxml.constants.md)

### Значення, що повертаються

Возвращает количество XInclude в документе, -1 если при обработке произошла ошибка, либо\*\*`false`\*\*, якщо не було зроблено жодної заміни.

### Приклади

**Приклад #1 Приклад використання DOMDocument::xinclude()**

```php
<?php

$xml = <<<EOD
<?xml version="1.0" ?>
<chapter xmlns:xi="http://www.w3.org/2001/XInclude">
 <title>Books of the other guy..</title>
 <para>
  <xi:include href="book.xml">
   <xi:fallback>
    <error>xinclude: book.xml not found</error>
   </xi:fallback>
  </xi:include>
 </para>
</chapter>
EOD;

$dom = new DOMDocument;

// оформим вывод красиво
$dom->preserveWhiteSpace = false;
$dom->formatOutput = true;

// загрузка XML-строки, определённой выше
$dom->loadXML($xml);

// вставка блоков xinclude
$dom->xinclude();

echo $dom->saveXML();

?>
```

Висновок наведеного прикладу буде схожим на:

```
<?xml version="1.0"?>
<chapter xmlns:xi="http://www.w3.org/2001/XInclude">
  <title>Books of the other guy..</title>
  <para>
    <row xml:base="/home/didou/book.xml">
       <entry>The Grapes of Wrath</entry>
       <entry>John Steinbeck</entry>
       <entry>en</entry>
       <entry>0140186409</entry>
      </row>
    <row xml:base="/home/didou/book.xml">
       <entry>The Pearl</entry>
       <entry>John Steinbeck</entry>
       <entry>en</entry>
       <entry>014017737X</entry>
      </row>
    <row xml:base="/home/didou/book.xml">
       <entry>Samarcande</entry>
       <entry>Amine Maalouf</entry>
       <entry>fr</entry>
       <entry>2253051209</entry>
      </row>
  </para>
</chapter>
```
