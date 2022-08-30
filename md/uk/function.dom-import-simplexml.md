Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement

-   [« Функции DOM](ref.dom.md)
    
-   [libxml »](book.libxml.md)
    
-   [PHP Manual](index.md)
    
-   [Функции DOM](ref.dom.md)
    
-   Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement
    

# domimportsimplexml

(PHP 5, PHP 7, PHP 8)

domimportsimplexml — Отримує об'єкт класу [DOMElement](class.domelement.md) з об'єкту класу [SimpleXMLElement](class.simplexmlelement.md)

### Опис

```methodsynopsis
dom_import_simplexml(object $node): DOMElement
```

Ця функція бере вузол `node` класу [SimpleXML](ref.simplexml.md) і перетворює його на вузол [DOMElement](class.domelement.md). Потім цей новий об'єкт може бути використаний як власний вузол [DOMElement](class.domelement.md)

### Список параметрів

`node`

Вузол [SimpleXMLElement](class.simplexmlelement.md)

### Значення, що повертаються

Доданий вузол [DOMElement](class.domelement.md)

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

-   [simplexmlimportdom()](function.simplexml-import-dom.html) - Отримує об'єкт класу SimpleXMLElement із вузла DOM