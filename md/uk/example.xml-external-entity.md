---
navigation:
  - example.xml-map-tags.md: « Приклад відображення тегів XML
  - ref.xml.md: Функції парсера XML »
  - index.md: PHP Manual
  - xml.examples.md: Приклади
title: Приклад використання зовнішніх сутностей XML
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Приклад використання зовнішніх сутностей XML

Цей приклад підсвічує XML-код. Він ілюструє те, як необхідно використовувати обробник посилання на зовнішню сутність для підключення і аналізу вмісту зовнішніх файлів, так само як може бути оброблений PI, і шлях для визначення "довіри" до коду, що міститься в PI.

XML документи, які використовуються в прикладі, розташовані під самим прикладом (xmltest.xml і xmltest2.xml.)

**Приклад #1 Приклад використання зовнішньої сутності**

```php
<?php
$file = "xmltest.xml";

function trustedFile($file)
{
    // доверять только нашим собственным локальным файлам
    if (!preg_match("@^([a-z][a-z0-9+.-]*)\:\/\/@i", $file)
        && fileowner($file) == getmyuid()) {
            return true;
    }
    return false;
}

function startElement($parser, $name, $attribs)
{
    echo "&lt;<font color=\"#0000cc\">$name</font>";
    if (count($attribs)) {
        foreach ($attribs as $k => $v) {
            echo " <font color=\"#009900\">$k</font>=\"<font
                   color=\"#990000\">$v</font>\"";
        }
    }
    echo "&gt;";
}

function endElement($parser, $name)
{
    echo "&lt;/<font color=\"#0000cc\">$name</font>&gt;";
}

function characterData($parser, $data)
{
    echo "<b>$data</b>";
}

function PIHandler($parser, $target, $data)
{
    switch (strtolower($target)) {
        case "php":
            global $parser_file;
            // Если обработанный документ является "доверенным", то можно сказать,
            // что запуск расположенного в нем кода является безопасным. Если нет,
            // то вместо запуска отобразить сам код.
            if (trustedFile($parser_file[$parser])) {
                eval($data);
            } else {
                printf("Небезопасный код PHP: <i>%s</i>",
                        htmlspecialchars($data));
            }
            break;
    }
}

function defaultHandler($parser, $data)
{
    if (substr($data, 0, 1) == "&" && substr($data, -1, 1) == ";") {
        printf('<font color="#aa00aa">%s</font>',
                htmlspecialchars($data));
    } else {
        printf('<font size="-1">%s</font>',
                htmlspecialchars($data));
    }
}

function externalEntityRefHandler($parser, $openEntityNames, $base, $systemId,
                                  $publicId) {
    if ($systemId) {
        if (!list($parser, $fp) = new_xml_parser($systemId)) {
            printf("Невозможно открыть сущность %s в %s\n", $openEntityNames,
                   $systemId);
            return false;
        }
        while ($data = fread($fp, 4096)) {
            if (!xml_parse($parser, $data, feof($fp))) {
                printf("Ошибка XML: %s в строке %d в процессе разбора сущности %s\n",
                       xml_error_string(xml_get_error_code($parser)),
                       xml_get_current_line_number($parser), $openEntityNames);
                xml_parser_free($parser);
                return false;
            }
        }
        xml_parser_free($parser);
        return true;
    }
    return false;
}

function new_xml_parser($file)
{
    global $parser_file;

    $xml_parser = xml_parser_create();
    xml_parser_set_option($xml_parser, XML_OPTION_CASE_FOLDING, 1);
    xml_set_element_handler($xml_parser, "startElement", "endElement");
    xml_set_character_data_handler($xml_parser, "characterData");
    xml_set_processing_instruction_handler($xml_parser, "PIHandler");
    xml_set_default_handler($xml_parser, "defaultHandler");
    xml_set_external_entity_ref_handler($xml_parser, "externalEntityRefHandler");

    if (!($fp = @fopen($file, "r"))) {
        return false;
    }
    if (!is_array($parser_file)) {
        settype($parser_file, "array");
    }
    $parser_file[$xml_parser] = $file;
    return array($xml_parser, $fp);
}

if (!(list($xml_parser, $fp) = new_xml_parser($file))) {
    die("Чтение XML-файла невозможно");
}

echo "<pre>";
while ($data = fread($fp, 4096)) {
    if (!xml_parse($xml_parser, $data, feof($fp))) {
        die(sprintf("Ошибка XML: %s в строке %d\n",
                    xml_error_string(xml_get_error_code($xml_parser)),
                    xml_get_current_line_number($xml_parser)));
    }
}
echo "</pre>";
echo "разбор завершён\n";
xml_parser_free($xml_parser);

?>
```

**Приклад #2 xmltest.xml**

\]> Title &plainEntity; a1b1c1 a2c2 a3b3c3 &systemEntity;

About this Document

Цей файл підключено до xmltest.xml:

**Приклад #3 xmltest2.xml**

\]> &testEnt;
