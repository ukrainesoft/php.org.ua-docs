---
navigation:
  - xmlreader.readouterxml.md: '« XMLReader::readOuterXml'
  - xmlreader.setparserproperty.md: 'XMLReader::setParserProperty »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::readString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::readString

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

XMLReader::readString — Прочитати вміст поточного вузла як рядок

### Опис

```methodsynopsis
public XMLReader::readString(): string
```

Читає вміст поточного вузла як рядок.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст поточного вузла у вигляді рядка. У разі виникнення помилки рядок буде порожнім.

### Примітки

**Застереження**

Ця функція доступна лише якщо PHP скомпільовано за допомогою libxml 20620 або старше.

### Дивіться також

-   [XMLReader::readOuterXml()](xmlreader.readouterxml.md) \- Отримати XML із поточного вузла, включаючи сам вузол
-   [XMLReader::readInnerXml()](xmlreader.readinnerxml.md) \- Вийняти XML із поточного вузла
-   [XMLReader::expand()](xmlreader.expand.md) \- Повернути копію поточного вузла у вигляді об'єкта DOM
