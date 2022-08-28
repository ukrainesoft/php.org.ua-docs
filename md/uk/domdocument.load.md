Завантаження XML із файлу

-   [« DOMDocument::importNode](domdocument.importnode.html)
    
-   [DOMDocument::loadHTML »](domdocument.loadhtml.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Завантаження XML із файлу
    

# DOMDocument::load

(PHP 5, PHP 7, PHP 8)

DOMDocument::load — Завантаження XML із файлу

### Опис

```methodsynopsis
public DOMDocument::load(string $filename, int $options = 0): DOMDocument|bool
```

Завантажує XML-документ із файлу.

**Увага**

Шляхи до файлів у стилі Unix із прямими слешами можуть негативно зашкодити працездатності скриптів серед Windows; використовуйте функцію [realpath()](function.realpath.html) для виключення подібних ситуацій.

### Список параметрів

`filename`

Шлях до документа XML.

`options`

[Побитовое `ИЛИ`](language.operators.bitwise.html) [констант опций libxml](libxml.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. При статичному виклику повертає об'єкт класу [DOMDocument](class.domdocument.html) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `filename` передано порожній рядок або файл нічого не містить, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблене обробниками помилок бібліотеки libxml.

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.html)

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->load('book.xml');
echo $doc->saveXML();
?>
```

### Дивіться також

-   [DOMDocument::loadXML()](domdocument.loadxml.html) - Завантаження XML з рядка
-   [DOMDocument::save()](domdocument.save.html) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveXML()](domdocument.savexml.html) - Зберігає XML-дерево з внутрішньої вистави у вигляді рядка