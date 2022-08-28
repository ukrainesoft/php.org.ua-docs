Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виведення

-   [« XMLWriter::openMemory](xmlwriter.openmemory.html)
    
-   [XMLWriter::outputMemory »](xmlwriter.outputmemory.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виведення
    

# XMLWriter::openUri

# xmlwriteropenuri

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::openUri -- xmlwriteropenuri — Створити новий об'єкт XMLWriter, використовуючи вихідний URI для виводу

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::openUri(string $uri): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_open_uri(string $uri): XMLWriter|false
```

Створює новий об'єкт [XMLWriter](class.xmlwriter.html), використовуючи `uri` для виведення.

### Список параметрів

`uri`

URI ресурс для виведення.

### Значення, що повертаються

Об'єктно-орієнтований стиль: Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Процедурний стиль: Повертає новий [XMLWriter](class.xmlwriter.html) для подальшого використання функціями xmlwriter у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                          |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Функція тепер повертає екземпляр [XMLWriter](class.xmlwriter.html) у разі успішного виконання. Раніше в цьому випадку повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Прямий висновок XML**

Можна безпосередньо виводити XML, використовуючи [обёртку потока php://output](wrappers.php.html#wrappers.php.output)

```php
<?php
$out =new XMLWriter();
$out->openURI('php://output');
?>
```

### Примітки

> **Зауваження**
> 
> У Windows файли, відкриті за допомогою цієї функції, блокуються доти, доки засіб запису не буде звільнено.

### Дивіться також

-   [XMLWriter::openMemory()](xmlwriter.openmemory.html) - Створити новий об'єкт XMLWriter, використовуючи пам'ять для рядкового виводу