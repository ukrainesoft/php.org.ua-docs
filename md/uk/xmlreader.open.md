Встановити URI, що містить XML-документ для аналізу

-   [« XMLReader::next](xmlreader.next.html)
    
-   [XMLReader::read »](xmlreader.read.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Встановити URI, що містить XML-документ для аналізу
    

# XMLReader::open

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

Кодування документа або **`null`**

`flags`

Бітова маска, що складається з [LIBXML\_\*](libxml.constants.html) констант.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. при статичному виклику, повертається [XMLReader](class.xmlreader.html) або **`false`** у разі виникнення помилки.

### Помилки

метод можна викликати статично, але до PHP 8.0.0 у цьому випадку видається помилка **`E_DEPRECATED`**

### список змін

| Версия | Описание |
| --- | --- |
|  | **XMLReader::open()** тепер оголошено як статичний метод, але все ще може бути викликаний в екземплярі [XMLReader](class.xmlreader.html) |

### Дивіться також

-   [XMLReader::xml()](xmlreader.xml.html) - Встановити дані, що містять XML для аналізу
-   [XMLReader::close()](xmlreader.close.html) - Закрити введення XMLReader