---
navigation:
  - xmlreader.getattributens.md: '« XMLReader::getAttributeNs'
  - xmlreader.isvalid.md: 'XMLReader::isValid »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getParserProperty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::getParserProperty

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::getParserProperty — Вказує, чи встановлено певну властивість.

### Опис

```methodsynopsis
public XMLReader::getParserProperty(int $property): bool
```

Вказує, чи була певна властивість встановлена.

### Список параметрів

`property`

Одна из[констант аналізатора](class.xmlreader.md#xmlreader.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XMLReader::setParserProperty()](xmlreader.setparserproperty.md) \- Встановлює опцію парсера
