---
navigation:
  - xmlwriter.writepi.md: '« XMLWriter::writePi'
  - book.xsl.md: XSL »
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::writeRaw'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::writeRaw

# xmlwriter\_write\_raw

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL xmlwriter >= 2.0.4)

XMLWriter::writeRaw -- xmlwriter\_write\_raw — Записати необроблений текст XML

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeRaw(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_raw(XMLWriter $writer, string $content): bool
```

Записує необроблений текст XML.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`content`

Текстовий рядок для запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::text()](xmlwriter.text.md) \- Записати текст
