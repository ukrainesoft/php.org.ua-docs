---
navigation:
  - xmlreader.read.md: '« XMLReader::read'
  - xmlreader.readouterxml.md: 'XMLReader::readOuterXml »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::readInnerXml'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::readInnerXml

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

XMLReader::readInnerXml — Вийняти XML із поточного вузла

### Опис

```methodsynopsis
public XMLReader::readInnerXml(): string
```

Читає вміст поточного вузла, включаючи дочірні вузли та розмітку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст поточного вузла у вигляді рядка. Порожній рядок повертається у разі виникнення помилки.

### Примітки

**Застереження**

Ця функція доступна лише якщо PHP скомпільовано за допомогою libxml 20620 або старше.

### Дивіться також

-   [XMLReader::readString()](xmlreader.readstring.md) \- Прочитати вміст поточного вузла як рядок
-   [XMLReader::readOuterXml()](xmlreader.readouterxml.md) \- Отримати XML із поточного вузла, включаючи сам вузол
-   [XMLReader::expand()](xmlreader.expand.md) \- Повернути копію поточного вузла у вигляді об'єкта DOM
