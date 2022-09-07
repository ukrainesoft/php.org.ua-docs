---
navigation:
  - xmlreader.setparserproperty.md: '« XMLReader::setParserProperty'
  - xmlreader.setrelaxngschemasource.md: 'XMLReader::setRelaxNGSchemaSource »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::setRelaxNGSchema'
---
# XMLReader::setRelaxNGSchema

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::setRelaxNGSchema — Встановити ім'я файлу або URI для схеми RelaxNG

### Опис

```methodsynopsis
public XMLReader::setRelaxNGSchema(?string $filename): bool
```

Встановлює ім'я файлу або URI для схеми RelaxNG, які використовуються під час перевірки.

### Список параметрів

`filename`

Ім'я файлу або URI, що вказує на схему RelaxNG.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::setRelaxNGSchemaSource()](xmlreader.setrelaxngschemasource.md) - Встановлює дані, що містять схему RelaxNG
-   [XMLReader::setSchema()](xmlreader.setschema.md) - Перевірити документ за допомогою XSD
-   [XMLReader::isValid()](xmlreader.isvalid.md) - Показати, чи розбирається документ синтаксично правильним
