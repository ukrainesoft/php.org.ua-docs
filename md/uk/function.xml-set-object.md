---
navigation:
  - function.xml-set-notation-decl-handler.md: « xml\_set\_notation\_decl\_handler
  - function.xml-set-processing-instruction-handler.md: xml\_set\_processing\_instruction\_handler »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_set\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_set\_object

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_set\_object — Використання XML-аналізатора всередині об'єкта

### Опис

```methodsynopsis
xml_set_object(XMLParser $parser, object $object): true
```

Ця функція дозволяє використовувати `parser` всередині об'єкту `object`. Усі callback-функції можуть бути встановлені функціями [xml\_set\_element\_handler()](function.xml-set-element-handler.md) і т.п. та використовуватись як методи об'єкта `object`

### Список параметрів

`parser`

Посилання на аналізатор XML.

`object`

Об'єкт, у якому використовуватиметься XML-аналізатор.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** xml\_set\_object()\*\*\*\*

```php
<?php
class CustomXMLParser
{
    private $parser;

    function __construct()
    {
        $this->parser = xml_parser_create();

        xml_set_object($this->parser, $this);
        xml_set_element_handler($this->parser, "tag_open", "tag_close");
        xml_set_character_data_handler($this->parser, "cdata");
    }

    function parse($data)
    {
        xml_parse($this->parser, $data);
    }

    function tag_open($parser, $tag, $attributes)
    {
        var_dump($tag, $attributes);
    }

    function cdata($parser, $cdata)
    {
        var_dump($cdata);
    }

    function tag_close($parser, $tag)
    {
        var_dump($tag);
    }

} // окончание определения класса xml

$xml_parser = new CustomXMLParser();
$xml_parser->parse("<A ID='hallo'>PHP</A>");
?>
```

Результат виконання наведеного прикладу:

```
string(1) "A"
array(1) {
  ["ID"]=>
  string(5) "hallo"
}
string(3) "PHP"
string(1) "A"
```
