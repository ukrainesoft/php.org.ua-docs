Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement

-   [« Функции DOM](ref.dom.html)
    
-   [libxml »](book.libxml.html)
    
-   [PHP Manual](index.html)
    
-   [Функции DOM](ref.dom.html)
    
-   Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement
    

# domimportsimplexml

(PHP 5, PHP 7, PHP 8)

domimportsimplexml — Отримує об'єкт класу [DOMElement](class.domelement.html) з об'єкту класу [SimpleXMLElement](class.simplexmlelement.html)

### Опис

```methodsynopsis
dom_import_simplexml(object $node): DOMElement
```

Ця функція бере вузол `node` класу [SimpleXML](ref.simplexml.html) і перетворює його на вузол [DOMElement](class.domelement.html). Потім цей новий об'єкт може бути використаний як власний вузол [DOMElement](class.domelement.html)

### Список параметрів

`node`

Вузол [SimpleXMLElement](class.simplexmlelement.html)

### Значення, що повертаються

Доданий вузол [DOMElement](class.domelement.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не повертає **`null`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Імпорт SimpleXML у DOM за допомогою функції **domimportsimplexml()****

```php
<?php

$sxe = simplexml_load_string('<books><book><title>чепуха</title></book></books>');

if ($sxe === false) {
    echo 'Ошибка при разборе документа';
    exit;
}

$dom_sxe = dom_import_simplexml($sxe);
if (!$dom_sxe) {
    echo 'Ошибка при преобразовании XML';
    exit;
}

$dom = new DOMDocument('1.0');
$dom_sxe = $dom->importNode($dom_sxe, true);
$dom_sxe = $dom->appendChild($dom_sxe);

echo $dom->saveXML();

?>
```

### Дивіться також

-   [simplexml\_import\_dom()](function.simplexml-import-dom.html) - Отримує об'єкт класу SimpleXMLElement із вузла DOM