---
navigation:
  - domdocument.importnode.md: '« DOMDocument::importNode'
  - domdocument.loadhtml.md: 'DOMDocument::loadHTML »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::load'
---
# DOMDocument::load

(PHP 5, PHP 7, PHP 8)

DOMDocument::load — Завантаження XML із файлу

### Опис

```methodsynopsis
public DOMDocument::load(string $filename, int $options = 0): DOMDocument|bool
```

Завантажує XML-документ із файлу.

**Увага**

Шляхи до файлів у стилі Unix із прямими слешами можуть негативно зашкодити працездатності скриптів серед Windows; використовуйте функцію [realpath()](function.realpath.md) для виключення подібних ситуацій.

### Список параметрів

`filename`

Шлях до документа XML.

`options`

[Побитовое`ИЛИ`](language.operators.bitwise.md) [констант опций libxml](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. При статичному виклику повертає об'єкт класу [DOMDocument](class.domdocument.md) або **`false`** у разі виникнення помилки.

### Помилки

Якщо через аргумент `filename` передано порожній рядок або файл нічого не містить, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблене обробниками помилок бібліотеки libxml.

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.md)

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

-   [DOMDocument::loadXML()](domdocument.loadxml.md) - Завантаження XML з рядка
-   [DOMDocument::save()](domdocument.save.md) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveXML()](domdocument.savexml.md) - Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
