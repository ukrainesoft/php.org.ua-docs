---
navigation:
  - ref.dom.md: « Функції DOM
  - book.libxml.md: libxml »
  - index.md: PHP Manual
  - ref.dom.md: Функції DOM
title: dom\_import\_simplexml
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dom\_import\_simplexml

(PHP 5, PHP 7, PHP 8)

dom\_import\_simplexml — Отримує об'єкт класу [DOMElement](class.domelement.md) з об'єкту класу [SimpleXMLElement](class.simplexmlelement.md)

### Опис

```methodsynopsis
dom_import_simplexml(object $node): DOMElement
```

Ця функція бере вузол `node`класса[SimpleXML](ref.simplexml.md) і перетворює його на вузол [DOMElement](class.domelement.md). Потім цей новий об'єкт може бути використаний як власний вузол [DOMElement](class.domelement.md)

### Список параметрів

`node`

Узел[SimpleXMLElement](class.simplexmlelement.md)

### Значення, що повертаються

Доданий вузол [DOMElement](class.domelement.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`null`\*\*в случае возникновения ошибки. |

### Приклади

**Приклад #1 Імпорт SimpleXML у DOM за допомогою функції **dom\_import\_simplexml()****

```php
<?php

$sxe = simplexml_load_string('<books><book><title>чепуха</title></book></books>');

if ($sxe === false) {
    echo 'Ошибка при разборе документа';
    exit;
}

$dom_sxe = dom_import_simplexml($sxe);
if (!$dom_sxe) {
    echo 'Ошибка при преобразовании XML';
    exit;
}

$dom = new DOMDocument('1.0');
$dom_sxe = $dom->importNode($dom_sxe, true);
$dom_sxe = $dom->appendChild($dom_sxe);

echo $dom->saveXML();

?>
```

### Дивіться також

-   [simplexml\_import\_dom()](function.simplexml-import-dom.md) \- Отримує об'єкт класу SimpleXMLElement із вузла DOM
