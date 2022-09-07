---
navigation:
  - function.xml-set-notation-decl-handler.md: « xmlsetnotationdeclhandler
  - function.xml-set-processing-instruction-handler.md: xmlsetprocessinginstructionhandler »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlsetobject
---
# xmlsetobject

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlsetobject — Використання XML-аналізатора всередині об'єкта

### Опис

```methodsynopsis
xml_set_object(XMLParser $parser, object $object): bool
```

Ця функція дозволяє використовувати `parser` всередині об'єкту `object`. Усі callback-функції можуть бути встановлені функціями [xmlsetelementhandler()](function.xml-set-element-handler.md) і т.п. та використовуватись як методи об'єкту `object`

### Список параметрів

`parser`

Посилання на аналізатор XML.

`object`

Об'єкт, у якому використовуватиметься XML-аналізатор.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **xmlsetobject()****

```php
<?php
class XMLParser
{
    private $parser;

    function __construct()
    {
        $this->parser = xml_parser_create();

        xml_set_object($this->parser, $this);
        xml_set_element_handler($this->parser, "tag_open", "tag_close");
        xml_set_character_data_handler($this->parser, "cdata");
    }

    function __destruct()
    {
        xml_parser_free($this->parser);
        unset($this->parser);
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

$xml_parser = new XMLParser();
$xml_parser->parse("<A ID='hallo'>PHP</A>");
?>
```

Результат виконання цього прикладу:

```
string(1) "A"
array(1) {
  ["ID"]=>
  string(5) "hallo"
}
string(3) "PHP"
string(1) "A"
```
