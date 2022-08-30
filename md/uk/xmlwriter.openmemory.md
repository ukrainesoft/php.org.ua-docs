Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу

-   [« XMLWriter::fullEndElement](xmlwriter.fullendelement.html)
    
-   [XMLWriter::openUri »](xmlwriter.openuri.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу
    

# XMLWriter::openMemory

# xmlwriteropenmemory

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::openMemory -- xmlwriteropenmemory — Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::openMemory(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_open_memory(): XMLWriter|false
```

Створює новий об'єкт [XMLWriter](class.xmlwriter.html), використовуючи пам'ять для рядкового виводу.

### Список параметрів

### Значення, що повертаються

Об'єктно-орієнтований стиль: Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Процедурний стиль: Повертає новий [XMLWriter](class.xmlwriter.html) для подальшого використання функціями xmlwriter у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція тепер повертає екземпляр [XMLWriter](class.xmlwriter.html) у разі успішного виконання. Раніше в цьому випадку повертався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [XMLWriter::openUri()](xmlwriter.openuri.html) - Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виведення