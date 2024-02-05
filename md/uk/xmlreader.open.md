---
navigation:
  - xmlreader.next.md: '« XMLReader::next'
  - xmlreader.read.md: 'XMLReader::read »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::open'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::open

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::open — Встановити URI, що містить XML-документ для аналізу

### Опис

```methodsynopsis
public static XMLReader::open(string $uri, ?string $encoding = null, int $flags = 0): bool|XMLReader
```

Встановити URI, що містить документ XML, який буде розібраний.

### Список параметрів

`uri`

URI, що вказує на документ.

`encoding`

Кодировка документа или\*\*`null`\*\*

`flags`

Бітова маска, що складається з [LIBXML\_\*](libxml.constants.md)констант.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. при статичному виклику, повертається [XMLReader](class.xmlreader.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

метод можна викликати статично, але до PHP 8.0.0 у цьому випадку видається помилка **`E_DEPRECATED`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **XMLReader::open()** тепер оголошено як статичний метод, але все ще може бути викликаний в екземплярі [XMLReader](class.xmlreader.md) |

### Дивіться також

-   [XMLReader::xml()](xmlreader.xml.md) \- Встановити дані, що містять XML для аналізу
-   [XMLReader::close()](xmlreader.close.md) \- Закрити введення XMLReader
