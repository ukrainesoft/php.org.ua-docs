---
navigation:
  - xmlwriter.writeattributens.md: '« XMLWriter::writeAttributeNs'
  - xmlwriter.writecomment.md: 'XMLWriter::writeComment »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeCdata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeCdata

# xmlwriter\_write\_cdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeCdata -- xmlwriter\_write\_cdata — Записати повний тег CDATA

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`content`

Вміст CDATA.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Приклади

**Пример #1 Базовое использование**xmlwriter\_write\_cdata()\*\*\*\*

```php
<?php
// настроить документ
$xml = new XmlWriter();
$xml->openMemory();
$xml->setIndent(true);
$xml->startDocument('1.0', 'UTF-8');
$xml->startElement('mydoc');
$xml->startElement('myele');

// вывод CData
$xml->startElement('mycdataelement');
$xml->writeCData("текст для включения как CData");
$xml->endElement();

// завершить документ и вывести
$xml->endElement();
$xml->endElement();
echo $xml->outputMemory(true);
?>
```

Результат виконання наведеного прикладу:

```
<mydoc>
 <myele>
  <mycdataelement><![CDATA[текст для включения как CData]​]></mycdataelement>
 </myele>
</mydoc>
```

### Дивіться також

-   [XMLWriter::startCdata()](xmlwriter.startcdata.md) \- Створити початковий тег CDATA
-   [XMLWriter::endCdata()](xmlwriter.endcdata.md) \- Завершити поточну секцію CDATA
