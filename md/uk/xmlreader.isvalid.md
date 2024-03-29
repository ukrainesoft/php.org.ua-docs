---
navigation:
  - xmlreader.getparserproperty.md: '« XMLReader::getParserProperty'
  - xmlreader.lookupnamespace.md: 'XMLReader::lookupNamespace »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::isValid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::isValid

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::isValid — Показати, чи є документ, що розбирається, синтаксично правильним

### Опис

```methodsynopsis
public XMLReader::isValid(): bool
```

Повертає логічне значення (boolean), яке є ознакою того, що документ, що розбирається, є синтаксично правильним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перевірка правильності XML**

```php
<?php
$xml = XMLReader::open('test.xml');

// Для работы метода обязательно должна быть включена
// валидация парсера.
$xml->setParserProperty(XMLReader::VALIDATE, true);

var_dump($xml->isValid());
?>
```

### Примітки

> **Зауваження**: Перевіряється лише поточна нода, а не весь документ.

### Дивіться також

-   [XMLReader::setParserProperty()](xmlreader.setparserproperty.md) \- Встановлює опцію парсера
-   [XMLReader::setRelaxNGSchema()](xmlreader.setrelaxngschema.md) \- Встановити ім'я файлу або URI для схеми RelaxNG
-   [XMLReader::setRelaxNGSchemaSource()](xmlreader.setrelaxngschemasource.md) \- Встановлює дані, що містять схему RelaxNG
-   [XMLReader::setSchema()](xmlreader.setschema.md) \- Перевірити документ за допомогою XSD
