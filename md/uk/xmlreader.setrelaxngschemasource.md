Встановлює дані, що містять схему RelaxNG

-   [« XMLReader::setRelaxNGSchema](xmlreader.setrelaxngschema.html)
    
-   [XMLReader::setSchema »](xmlreader.setschema.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Встановлює дані, що містять схему RelaxNG
    

# XMLReader::setRelaxNGSchemaSource

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::setRelaxNGSchemaSource — Встановлює дані, що містять схему RelaxNG

### Опис

```methodsynopsis
public XMLReader::setRelaxNGSchemaSource(?string $source): bool
```

Встановлює дані, що містять схему RelaxNG, що використовується під час перевірки.

### Список параметрів

`source`

Рядок, що містить схему RelaxNG.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::setRelaxNGSchema()](xmlreader.setrelaxngschema.html) - Встановити ім'я файлу або URI для схеми RelaxNG
-   [XMLReader::setSchema()](xmlreader.setschema.html) - Перевірити документ за допомогою XSD
-   [XMLReader::isValid()](xmlreader.isvalid.html) - Показати, чи розбирається документ синтаксично правильним