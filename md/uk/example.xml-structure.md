Приклад Структури Елементу XML

-   [« Приклади](xml.examples.html)
    
-   [Пример отображения XML тегов »](example.xml-map-tags.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](xml.examples.html)
    
-   Приклад Структури Елементу XML
    

## Приклад Структури Елементу XML

Перший приклад відображає структуру початкових елементів документа з відступом.

**Приклад #1 Показати структуру елемента XML**

```php
<?php
$file = "data.xml";
$depth = 0;
function startElement($parser, $name, $attrs)
{
    global $depth;
    for ($i = 0; $i < $depth; $i++) {
        echo "  ";
    }
    echo "$name\n";
    $depth++;
}
function endElement($parser, $name)
{
    global $depth;
    $depth--;
}

$xml_parser = xml_parser_create();
xml_set_element_handler($xml_parser, "startElement", "endElement");
if (!($fp = fopen($file, "r"))) {
    die("Невозможно произвести чтение XML");
}

while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("Ошибка XML: %s на строке %d",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
xml_parser_free($xml_parser);
?>
```