Записати текст

-   [« XMLWriter::startPi](xmlwriter.startpi.html)
    
-   [XMLWriter::writeAttribute »](xmlwriter.writeattribute.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати текст
    

# XMLWriter::text

# xmlwritertext

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::text -- xmlwritertext — Записати текст

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::text(string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_text(XMLWriter $writer, string $content): bool
```

Записує текст.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`content`

Зміст тексту. Символи `<` `>` `&` і `"` записуються як посилання на сутність (тобто . `&lt;` `&gt;` `&amp;` і `&quot;`відповідно). Всі інші символи у тому числі `'` записуються буквально. Щоб записувати спеціальні символи XML буквально або записувати буквальні посилання на сутності, необхідно використовувати [xmlwriterwriteraw()](xmlwriter.writeraw.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |