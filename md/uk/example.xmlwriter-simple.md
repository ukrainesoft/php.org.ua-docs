Створення простого XML-документа

-   [« Приклади](xmlwriter.examples.html)
    
-   [Робота з просторами імен XML »](example.xmlwriter-namespace.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](xmlwriter.examples.html)
    
-   Створення простого XML-документа
    

## Створення простого XML-документа

Цей приклад демонструє створення XML-документа у пам'яті за допомогою XMLWriter.

**Приклад #1 Створення простого документа XML**

```php
<?php

$xw = xmlwriter_open_memory();
xmlwriter_set_indent($xw, 1);
$res = xmlwriter_set_indent_string($xw, ' ');

xmlwriter_start_document($xw, '1.0', 'UTF-8');

// Первый элемент
xmlwriter_start_element($xw, 'tag1');

// Атрибут 'att1' для элемента 'tag1'
xmlwriter_start_attribute($xw, 'att1');
xmlwriter_text($xw, 'valueofatt1');
xmlwriter_end_attribute($xw);

xmlwriter_write_comment($xw, 'this is a comment.');

// Создаём дочерний элемент
xmlwriter_start_element($xw, 'tag11');
xmlwriter_text($xw, 'This is a sample text, ä');
xmlwriter_end_element($xw); // tag11

xmlwriter_end_element($xw); // tag1


// CDATA
xmlwriter_start_element($xw, 'testc');
xmlwriter_write_cdata($xw, "This is cdata content");
xmlwriter_end_element($xw); // testc

xmlwriter_start_element($xw, 'testc');
xmlwriter_start_cdata($xw);
xmlwriter_text($xw, "test cdata2");
xmlwriter_end_cdata($xw);
xmlwriter_end_element($xw); // testc

// Инструкции по обработке
xmlwriter_start_pi($xw, 'php');
xmlwriter_text($xw, '$foo=2;echo $foo;');
xmlwriter_end_pi($xw);

xmlwriter_end_document($xw);

echo xmlwriter_output_memory($xw);
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="UTF-8"?>
<tag1 att1="valueofatt1">
 <!--this is a comment.-->
 <tag11>This is a sample text, ä</tag11>
</tag1>
<testc><![CDATA[This is cdata content]]></testc>
<testc><![CDATA[test cdata2]]></testc>
<?php $foo=2;echo $foo;?>
```