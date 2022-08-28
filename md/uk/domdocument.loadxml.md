Завантаження XML з рядка

-   [« DOMDocument::loadHTMLFile](domdocument.loadhtmlfile.html)
    
-   [DOMDocument::normalizeDocument »](domdocument.normalizedocument.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Завантаження XML з рядка
    

# DOMDocument::loadXML

(PHP 5, PHP 7, PHP 8)

DOMDocument::loadXML — Завантаження XML з рядка

### Опис

```methodsynopsis
public DOMDocument::loadXML(string $source, int $options = 0): DOMDocument|bool
```

Завантажує XML-документ із рядка.

### Список параметрів

`source`

Містить XML-рядок.

`options`

[Побитовое `ИЛИ`](language.operators.bitwise.html) [констант опций libxml](libxml.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо викликана статично, повертає об'єкт класу [DOMDocument](class.domdocument.html) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `source` передано порожній рядок, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено функціями обробки помилок libxml.

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.html)

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->loadXML('<root><node/></root>');
echo $doc->saveXML();
?>
```

**Приклад #2 Статичний виклик `loadXML`**

```php
<?php
// Вызывает ошибку E_DEPRECATED
$doc = DOMDocument::loadXML('<root><node/></root>');
echo $doc->saveXML();
?>
```

### Дивіться також

-   [DOMDocument::load()](domdocument.load.html) - Завантаження XML із файлу
-   [DOMDocument::save()](domdocument.save.html) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveXML()](domdocument.savexml.html) - Зберігає XML-дерево з внутрішньої вистави у вигляді рядка