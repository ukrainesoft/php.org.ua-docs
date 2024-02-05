---
navigation:
  - domcharacterdata.replacedata.md: '« DOMCharacterData::replaceData'
  - domcharacterdata.substringdata.md: 'DOMCharacterData::substringData »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::replaceWith'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::replaceWith

(PHP 8)

DOMCharacterData::replaceWith — Замінює символьні дані новими вузлами

### Опис

```methodsynopsis
public DOMCharacterData::replaceWith(DOMNode|string ...$nodes): void
```

Замінює символьні дані новими вузлами `nodes`

### Список параметрів

`nodes`

Вузли для заміни. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі батьківського вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик методу на вузлі без батька тепер заборонено, щоб привести поведінку у відповідність до специфікації DOM. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Приклад #1 Приклад использования метода**DOMCharacterData::replaceWith()\*\*\*\*

Заміна символьних даних на нові вузли.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><![CDATA[hello]]></container>");
$cdata = $doc->documentElement->firstChild;

$cdata->replaceWith("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container>beautiful<world/></container>
```

### Дивіться також

-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) \- Замінює вузол на нові вузли
-   [DOMCharacterData::after()](domcharacterdata.after.md) \- Додає вузли після символьних даних
-   [DOMCharacterData::before()](domcharacterdata.before.md) \- Додає вузли перед вузлом
-   [DOMCharacterData::remove()](domcharacterdata.remove.md) \- Видаляє символьні дані
