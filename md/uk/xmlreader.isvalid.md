Показати, чи розбирається документ синтаксично правильним

-   [« XMLReader::getParserProperty](xmlreader.getparserproperty.html)
    
-   [XMLReader::lookupNamespace »](xmlreader.lookupnamespace.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Показати, чи розбирається документ синтаксично правильним
    

# XMLReader::isValid

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::isValid — Показати, чи є документ, що розбирається, синтаксично правильним

### Опис

```methodsynopsis
public XMLReader::isValid(): bool
```

Повертає логічне значення (boolean), яке є ознакою того, що документ, що розбирається, є синтаксично правильним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перевірка правильності XML**

```php
<?php
$xml = XMLReader::open('test.xml');

// Для работы метода обязательно должна быть включена
// валидация парсера.
$xml->setParserProperty(XMLReader::VALIDATE, true);

var_dump($xml->isValid());
?>
```

### Примітки

> **Зауваження**: Перевіряється лише поточна нода, а не весь документ.

### Дивіться також

-   [XMLReader::setParserProperty()](xmlreader.setparserproperty.html) - Встановлює опцію парсера
-   [XMLReader::setRelaxNGSchema()](xmlreader.setrelaxngschema.html) - Встановити ім'я файлу або URI для схеми RelaxNG
-   [XMLReader::setRelaxNGSchemaSource()](xmlreader.setrelaxngschemasource.html) - Встановлює дані, що містять схему RelaxNG
-   [XMLReader::setSchema()](xmlreader.setschema.html) - Перевірити документ за допомогою XSD