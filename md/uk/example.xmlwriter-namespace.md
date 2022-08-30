Робота з просторами імен XML

-   [« Створення простого XML-документу](example.xmlwriter-simple.html)
    
-   [Робота з об'єктно-орієнтованим API »](example.xmlwriter-oop.html)
    
-   [PHP Manual](index.html)
    
-   [Приклади](xmlwriter.examples.html)
    
-   Робота з просторами імен XML
    

## Робота з просторами імен XML

У цьому прикладі демонструється створення елементів просторі імен.

**Приклад #1 Робота з просторами імен XML**

```php
<?php

$xw = xmlwriter_open_memory();
xmlwriter_set_indent($xw, 1);
$res = xmlwriter_set_indent_string($xw, ' ');

xmlwriter_start_document($xw, '1.0', 'UTF-8');
// Первый элемент
xmlwriter_start_element_ns($xw,'prefix', 'books', 'uri');
xmlwriter_start_attribute($xw, 'isbn');

xmlwriter_start_attribute_ns($xw, 'prefix', 'isbn', 'uri');
xmlwriter_end_attribute($xw);

xmlwriter_end_attribute($xw);

xmlwriter_text($xw, 'book1');
xmlwriter_end_element($xw);

xmlwriter_end_document($xw);

echo xmlwriter_output_memory($xw);
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="UTF-8"?>
<prefix:books isbn="" prefix:isbn="" xmlns:prefix="uri">book1</prefix:books>
```