---
navigation:
  - xmlreader.getattributens.md: '« XMLReader::getAttributeNs'
  - xmlreader.isvalid.md: 'XMLReader::isValid »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getParserProperty'
---
# XMLReader::getParserProperty

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::getParserProperty — Вказує, чи встановлено певну властивість.

### Опис

```methodsynopsis
public XMLReader::getParserProperty(int $property): bool
```

Вказує, чи була певна властивість встановлена.

### Список параметрів

`property`

Одна з [констант аналізатора](class.xmlreader.md#xmlreader.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::setParserProperty()](xmlreader.setparserproperty.md) - Встановлює опцію парсера
