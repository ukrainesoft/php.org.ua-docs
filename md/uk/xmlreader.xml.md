Встановити дані, що містять XML для аналізу

-   [« XMLReader::setSchema](xmlreader.setschema.html)
    
-   [XMLWriter »](book.xmlwriter.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Встановити дані, що містять XML для аналізу
    

# XMLReader::XML

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

Кодування документа або **`null`**

`flags`

Бітова маска констант [LIBXML](libxml.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. у разі статичного виклику або повертається [XMLReader](class.xmlreader.html) або **`false`** у разі виникнення помилки.

### Помилки

Метод можна викликати статично, але до PHP 8.0.0 у цьому випадку видається помилка **`E_DEPRECATED`**

### список змін

| Версия | Описание                                                                                                                                |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
|        | **XMLReader::XML()** тепер оголошено як статичний метод, але все ще може бути викликаний в екземплярі [XMLReader](class.xmlreader.html) |

### Дивіться також

-   [XMLReader::open()](xmlreader.open.html) - Встановити URI, що містить XML-документ для аналізу
-   [XMLReader::close()](xmlreader.close.html) - Закрити введення XMLReader