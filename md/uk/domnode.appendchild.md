Додає новий дочірній вузол до кінця списку нащадків

-   [« DOMNode](class.domnode.md)
    
-   [DOMNode::C14N »](domnode.c14n.md)
    
-   [PHP Manual](index.md)
    
-   [DOMNode](class.domnode.md)
    
-   Додає новий дочірній вузол до кінця списку нащадків
    

# DOMNode::appendChild

(PHP 5, PHP 7, PHP 8)

DOMNode::appendChild — Додає новий дочірній вузол до кінця списку нащадків.

### Опис

```methodsynopsis
public DOMNode::appendChild(DOMNode $node): DOMNode|false
```

Функція додає дочірній вузол до існуючого списку нащадків або створює новий список дочірніх елементів. Дочірній вузол може бути створений за допомогою [DOMDocument::createElement()](domdocument.createelement.md) [DOMDocument::createTextNode()](domdocument.createtextnode.md) і т.д., або може бути використаний будь-який інший вузол.

При використанні існуючого вузла його буде переміщено.

### Список параметрів

`node`

Дочірній вузол, що додається.

### Значення, що повертаються

Доданий вузол.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний тільки для читання або попередній батько вузла, що вставляється, доступний тільки для читання.

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип вузла не підтримує нащадків типу, що має вузол `node`, або якщо вузол, що додається, є одним з предком цільового вузла або ним самим.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо `node` створено іншому документі, відмінному від цього, у якому було створено цей вузол.

### Приклади

Наступний приклад додає новий вузол у щойно створений документ.

**Приклад #1 Додавання дочірнього вузла**

```php
<?php

$doc = new DOMDocument;

$node = $doc->createElement("para");
$newnode = $doc->appendChild($node);

echo $doc->saveXML();
?>
```

**Приклад #2 Вкладені дочірні вузли**

```php
<?php

$doc = new DOMDocument;

$headNode = $doc->createElement("head");
$doc->appendChild($headNode);

$titleNode = $doc->createElement("title");
$headNode->appendChild($titleNode);

echo $doc->saveXML();
?>
```

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) - Додає вузли після вузла
-   [DOMNode::insertBefore()](domnode.insertbefore.md) - Додає новий дочірній вузол перед вказаним вузлом
-   [DOMNode::removeChild()](domnode.removechild.md) - видаляє дочірній вузол зі списку нащадків
-   [DOMNode::replaceChild()](domnode.replacechild.md) - Замінює дочірній вузол