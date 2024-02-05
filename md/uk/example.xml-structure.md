---
navigation:
  - xml.examples.md: « Приклади
  - example.xml-map-tags.md: Приклад відображення тегів XML »
  - index.md: PHP Manual
  - xml.examples.md: Приклади
title: Приклад Структури Елементу XML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Приклад Структури Елементу XML

Перший приклад відображає структуру початкових елементів документа з відступом.

**Приклад #1 Показати структуру елемента XML**

```php
<?php
$file = "data.xml";
$depth = 0;
function startElement($parser, $name, $attrs)
{
    global $depth;
    for ($i = 0; $i < $depth; $i++) {
        echo "  ";
    }
    echo "$name\n";
    $depth++;
}
function endElement($parser, $name)
{
    global $depth;
    $depth--;
}

$xml_parser = xml_parser_create();
xml_set_element_handler($xml_parser, "startElement", "endElement");
if (!($fp = fopen($file, "r"))) {
    die("Невозможно произвести чтение XML");
}

while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("Ошибка XML: %s на строке %d",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
xml_parser_free($xml_parser);
?>
```
