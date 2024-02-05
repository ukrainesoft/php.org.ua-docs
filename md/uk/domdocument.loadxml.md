---
navigation:
  - domdocument.loadhtmlfile.md: '« DOMDocument::loadHTMLFile'
  - domdocument.normalizedocument.md: 'DOMDocument::normalizeDocument »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::loadXML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::loadXML

(PHP 5, PHP 7, PHP 8)

DOMDocument::loadXML — Завантаження XML з рядка

### Опис

```methodsynopsis
public DOMDocument::loadXML(string $source, int $options = 0): bool
```

Завантажує XML-документ із рядка.

### Список параметрів

`source`

Містить XML-рядок.

`options`

[Побитовое`АБО`](language.operators.bitwise.md) [констант опцій libxml](libxml.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо через аргумент `source` передано порожній рядок, буде згенеровано попередження. Це попередження не генерується libxml, тому воно не може бути оброблено функціями обробки помилок libxml.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер функція має попередній логічний (bool) тип значення, що повертається. |
| 8.0.0 | При статичному виклику функції тепер викидається помилка [Error](class.error.md). . Раніше видавалася помилка рівня **`E_DEPRECATED`** |

### Приклади

**Приклад #1 Створення документа**

```php
<?php
$doc = new DOMDocument();
$doc->loadXML('<root><node/></root>');
echo $doc->saveXML();
?>
```

### Дивіться також

-   [DOMDocument::load()](domdocument.load.md) \- Завантаження XML із файлу
-   [DOMDocument::save()](domdocument.save.md) \- Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::saveXML()](domdocument.savexml.md) \- Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
