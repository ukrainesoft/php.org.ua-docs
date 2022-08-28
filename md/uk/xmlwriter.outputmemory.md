Повертає поточний буфер

-   [« XMLWriter::openUri](xmlwriter.openuri.html)
    
-   [XMLWriter::setIndent »](xmlwriter.setindent.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Повертає поточний буфер
    

# XMLWriter::outputMemory

# xmlwriteroutputmemory

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::outputMemory -- xmlwriteroutputmemory — Повертає поточний буфер

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::outputMemory(bool $flush = true): string
```

Процедурний стиль

```methodsynopsis
xmlwriter_output_memory(XMLWriter $writer, bool $flush = true): string
```

Повертає поточний буфер.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`flush`

Визначає, чи звільнити буфер чи ні. За замовчуванням **`true`**

### Значення, що повертаються

Повертає поточний буфер у вигляді рядка.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::flush()](xmlwriter.flush.html) - Скинути поточний буфер