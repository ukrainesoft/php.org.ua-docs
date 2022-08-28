Завершити поточну секцію CDATA

-   [« XMLWriter::endAttribute](xmlwriter.endattribute.html)
    
-   [XMLWriter::endComment »](xmlwriter.endcomment.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточну секцію CDATA
    

# XMLWriter::endCdata

# xmlwriterendcdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endCdata -- xmlwriterendcdata — Завершити поточну секцію CDATA

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endCdata(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_cdata(XMLWriter $writer): bool
```

Завершує поточну секцію CDATA.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startCdata()](xmlwriter.startcdata.html) - Створити початковий тег CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.html) - Записати повний тег CDATA