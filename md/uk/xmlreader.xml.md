---
navigation:
  - xmlreader.setschema.md: '« XMLReader::setSchema'
  - book.xmlwriter.md: XMLWriter »
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::XML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::XML

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::XML — Встановити дані, що містять XML для аналізу

### Опис

```methodsynopsis
public static XMLReader::XML(string $source, ?string $encoding = null, int $flags = 0): bool|XMLReader
```

Встановлює дані, що містять XML для аналізу.

### Список параметрів

`source`

Рядок, що містить XML для аналізу.

`encoding`

Кодировка документа или\*\*`null`\*\*

`flags`

Битовая маска констант[LIBXML\_\*](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. у разі статичного виклику або повертається [XMLReader](class.xmlreader.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод можна викликати статично, але до PHP 8.0.0 у цьому випадку видається помилка **`E_DEPRECATED`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | **XMLReader::XML()** тепер оголошено як статичний метод, але все ще може бути викликаний в екземплярі [XMLReader](class.xmlreader.md) |

### Дивіться також

-   [XMLReader::open()](xmlreader.open.md) \- Встановити URI, що містить XML-документ для аналізу
-   [XMLReader::close()](xmlreader.close.md) \- Закрити введення XMLReader
