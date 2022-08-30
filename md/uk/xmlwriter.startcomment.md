Створює стартовий коментар

-   [« XMLWriter::startCdata](xmlwriter.startcdata.html)
    
-   [XMLWriter::startDocument »](xmlwriter.startdocument.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створює стартовий коментар
    

# XMLWriter::startComment

# xmlwriterstartcomment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::startComment -- xmlwriterstartcomment — Створює стартовий коментар

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startComment(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_comment(XMLWriter $writer): bool
```

Починає коментар.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endComment()](xmlwriter.endcomment.html) - Завершити коментар
-   [XMLWriter::writeComment()](xmlwriter.writecomment.html) - Записати повний тег коментаря