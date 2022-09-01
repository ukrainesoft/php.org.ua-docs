---
navigation:
  - xmlwriter.writeattributens.html: '« XMLWriter::writeAttributeNs'
  - xmlwriter.writecomment.html: 'XMLWriter::writeComment »'
  - index.html: PHP Manual
  - class.xmlwriter.html: XMLWriter
title: 'XMLWriter::writeCdata'
---
# XMLWriter::writeCdata

# xmlwriterwritecdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeCdata -- xmlwriterwritecdata — Записати повний тег CDATA

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeCdata(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_cdata(XMLWriter $writer, string $content): bool
```

Записує повний CDTA тег.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`content`

Вміст CDATA.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Базове використання **xmlwriterwritecdata()****

```php
<?php
// настроить документ
$xml = new XmlWriter();
$xml->openMemory();
$xml->setIndent(true);
$xml->startDocument('1.0', 'UTF-8');
$xml->startElement('mydoc');
$xml->startElement('myele');

// вывод CData
$xml->startElement('mycdataelement');
$xml->writeCData("текст для включения как CData");
$xml->endElement();

// завершить документ и вывести
$xml->endElement();
$xml->endElement();
echo $xml->outputMemory(true);
?>
```

Результат виконання цього прикладу:

```
<mydoc>
 <myele>
  <mycdataelement><![CDATA[текст для включения как CData]​]></mycdataelement>
 </myele>
</mydoc>
```

### Дивіться також

-   [XMLWriter::startCdata()](xmlwriter.startcdata.md) - Створити початковий тег CDATA
-   [XMLWriter::endCdata()](xmlwriter.endcdata.md) - Завершити поточну секцію CDATA
