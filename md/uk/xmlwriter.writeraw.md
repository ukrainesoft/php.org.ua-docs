Записати необроблений XML-текст

-   [« XMLWriter::writePi](xmlwriter.writepi.html)
    
-   [XSL »](book.xsl.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати необроблений XML-текст
    

# XMLWriter::writeRaw

# xmlwriterwriteraw

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL xmlwriter >= 2.0.4)

XMLWriter::writeRaw -- xmlwriterwriteraw — Записати необроблений текст XML

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeRaw(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_raw(XMLWriter $writer, string $content): bool
```

Записує необроблений текст XML.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`content`

Текстовий рядок для запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::text()](xmlwriter.text.html) - Записати текст