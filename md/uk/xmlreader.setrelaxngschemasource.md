---
navigation:
  - xmlreader.setrelaxngschema.md: '« XMLReader::setRelaxNGSchema'
  - xmlreader.setschema.md: 'XMLReader::setSchema »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::setRelaxNGSchemaSource'
---
# XMLReader::setRelaxNGSchemaSource

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::setRelaxNGSchemaSource — Встановлює дані, що містять схему RelaxNG

### Опис

```methodsynopsis
public XMLReader::setRelaxNGSchemaSource(?string $source): bool
```

Встановлює дані, що містять схему RelaxNG, що використовується під час перевірки.

### Список параметрів

`source`

Рядок, що містить схему RelaxNG.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::setRelaxNGSchema()](xmlreader.setrelaxngschema.md) - Встановити ім'я файлу або URI для схеми RelaxNG
-   [XMLReader::setSchema()](xmlreader.setschema.md) - Перевірити документ за допомогою XSD
-   [XMLReader::isValid()](xmlreader.isvalid.md) - Показати, чи розбирається документ синтаксично правильним
