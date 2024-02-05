---
navigation:
  - xmlreader.readstring.md: '« XMLReader::readString'
  - xmlreader.setrelaxngschema.md: 'XMLReader::setRelaxNGSchema »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::setParserProperty'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::setParserProperty

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::setParserProperty — Встановлює опцію парсера

### Опис

```methodsynopsis
public XMLReader::setParserProperty(int $property, bool $value): bool
```

Встановлює настройки для парсера. Опції мають бути встановлені після виклику [XMLReader::open()](xmlreader.open.md) або [XMLReader::xml()](xmlreader.xml.md) та до першого виклику [XMLReader::read()](xmlreader.read.md)

### Список параметрів

`property`

Одна из[констант опцій парсеру](class.xmlreader.md#xmlreader.constants)

`value`

Если установлено в\*\*`true`\*\*, то опція буде включена, інакше опція буде вимкнена.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
