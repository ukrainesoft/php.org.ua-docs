Робота з об'єктно-орієнтованим API

-   [« Работа с пространствами имён XML](example.xmlwriter-namespace.html)
    
-   [XMLWriter »](class.xmlwriter.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](xmlwriter.examples.html)
    
-   Робота з об'єктно-орієнтованим API
    

## Робота з об'єктно-орієнтованим API

У цьому прикладі демонструється робота з об'єктно-орієнтованим API XMLWriter.

**Приклад #1 Робота з об'єктно-орієнтованим API**

```php
<?php

$xw = new XMLWriter();
$xw->openMemory();
$xw->startDocument("1.0");
$xw->startElement("book");
$xw->text("example");
$xw->endElement();
$xw->endDocument();
echo $xw->outputMemory();
```

Результат виконання цього прикладу:

```
<?xml version="1.0"?>
<book>example</book>
```