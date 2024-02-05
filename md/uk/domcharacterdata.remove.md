---
navigation:
  - domcharacterdata.insertdata.md: '« DOMCharacterData::insertData'
  - domcharacterdata.replacedata.md: 'DOMCharacterData::replaceData »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::remove

(PHP 8)

DOMCharacterData::remove — Видалення символьних даних

### Опис

```methodsynopsis
public DOMCharacterData::remove(): void
```

Видалення символьних даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования метода**DOMCharacterData::remove()\*\*\*\*

Видалення символьних даних.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><![CDATA[hello]]><world/></container>");
$cdata = $doc->documentElement->firstChild;

$cdata->remove();

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container><world/></container>
```

### Дивіться також

-   [DOMChildNode::remove()](domchildnode.remove.md) \- видаляє вузол
-   [DOMCharacterData::after()](domcharacterdata.after.md) \- Додає вузли після символьних даних
-   [DOMCharacterData::before()](domcharacterdata.before.md) \- Додає вузли перед вузлом
-   [DOMCharacterData::replaceWith()](domcharacterdata.replacewith.md) \- Замінює символьні дані новими вузлами
-   [DOMNode::removeChild()](domnode.removechild.md) \- видаляє дочірній вузол зі списку нащадків
