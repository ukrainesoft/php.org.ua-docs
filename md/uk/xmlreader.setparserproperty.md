---
navigation:
  - xmlreader.readstring.html: '« XMLReader::readString'
  - xmlreader.setrelaxngschema.html: 'XMLReader::setRelaxNGSchema »'
  - index.html: PHP Manual
  - class.xmlreader.html: XMLReader
title: 'XMLReader::setParserProperty'
---
# XMLReader::setParserProperty

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::setParserProperty — Встановлює опцію парсера

### Опис

```methodsynopsis
public
   XMLReader::setParserProperty(int $property, bool $value): bool
```

Встановлює настройки для парсера. Опції мають бути встановлені після виклику [XMLReader::open()](xmlreader.open.html) або [XMLReader::xml()](xmlreader.xml.html) та до першого виклику [XMLReader::read()](xmlreader.read.md)

### Список параметрів

`property`

Одна з [констант опций парсера](class.xmlreader.html#xmlreader.constants)

`value`

Якщо встановлено **`true`**, то опція буде включена, інакше опція буде вимкнена.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
