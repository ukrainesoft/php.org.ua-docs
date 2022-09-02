---
navigation:
  - xmlreader.readinnerxml.md: '« XMLReader::readInnerXml'
  - xmlreader.readstring.md: 'XMLReader::readString »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::readOuterXml'
---
# XMLReader::readOuterXml

(PHP 5> = 5.2.0, PHP 7, PHP 8)

XMLReader::readOuterXml — Отримати XML із поточного вузла, включаючи сам вузол

### Опис

```methodsynopsis
public XMLReader::readOuterXml(): string
```

Читає вміст поточного вузла, включаючи вузол.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст поточного вузла, включаючи сам вузол як рядок. У разі виникнення помилки рядок буде порожнім.

### Примітки

**Застереження**

Ця функція доступна лише якщо PHP скомпільовано за допомогою libxml 20620 або старше.

### Дивіться також

-   [XMLReader::readString()](xmlreader.readstring.md) - Прочитати вміст поточного вузла як рядок
-   [XMLReader::readInnerXml()](xmlreader.readinnerxml.md) - Вийняти XML із поточного вузла
-   [XMLReader::expand()](xmlreader.expand.md) - Повернути копію поточного вузла у вигляді об'єкта DOM
