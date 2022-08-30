Завантаження XML з рядка

-   [« DOMDocument::loadHTMLFile](domdocument.loadhtmlfile.md)
    
-   [DOMDocument::normalizeDocument »](domdocument.normalizedocument.md)
    
-   [PHP Manual](index.md)
    
-   [DOMDocument](class.domdocument.md)
    
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

[Побитовое`ИЛИ`](language.operators.bitwise.md) [констант опций libxml](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо викликана статично, повертає об'єкт класу [DOMDocument](class.domdocument.md) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `source` передано порожній рядок, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено функціями обробки помилок libxml.

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.md)

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

-   [DOMDocument::load()](domdocument.load.md) - Завантаження XML із файлу
-   [DOMDocument::save()](domdocument.save.md) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveXML()](domdocument.savexml.md) - Зберігає XML-дерево з внутрішньої вистави у вигляді рядка