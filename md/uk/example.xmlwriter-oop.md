---
navigation:
  - example.xmlwriter-namespace.md: Робота з просторами імен XML
  - class.xmlwriter.md: XMLWriter »
  - index.md: PHP Manual
  - xmlwriter.examples.md: Приклади
title: Робота з об'єктно-орієнтованим API
---
## Робота з об'єктно-орієнтованим API

У цьому прикладі демонструється робота з об'єктно-орієнтованим API XMLWriter.

**Приклад #1 Робота з об'єктно-орієнтованим API**

```php
<?php

$xw = new XMLWriter();
$xw->openMemory();
$xw->startDocument("1.0");
$xw->startElement("book");
$xw->text("example");
$xw->endElement();
$xw->endDocument();
echo $xw->outputMemory();
```

Результат виконання цього прикладу:

```
<?xml version="1.0"?>
<book>example</book>
```
