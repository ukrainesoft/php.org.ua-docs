Створити початковий тег CDATA

-   [« XMLWriter::startAttributeNs](xmlwriter.startattributens.html)
    
-   [XMLWriter::startComment »](xmlwriter.startcomment.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити початковий тег CDATA
    

# XMLWriter::startCdata

# xmlwriterstartcdata

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startCdata -- xmlwriterstartcdata — Створити початковий тег CDATA

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startCdata(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_cdata(XMLWriter $writer): bool
```

Починає CDATA.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endCdata()](xmlwriter.endcdata.html) - Завершити поточну секцію CDATA
-   [XMLWriter::writeCdata()](xmlwriter.writecdata.html) - Записати повний тег CDATA