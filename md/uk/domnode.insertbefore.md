---
navigation:
  - domnode.haschildnodes.md: '« DOMNode::hasChildNodes'
  - domnode.isdefaultnamespace.md: 'DOMNode::isDefaultNamespace »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::insertBefore'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::insertBefore

(PHP 5, PHP 7, PHP 8)

DOMNode::insertBefore — Додає новий дочірній вузол перед вказаним вузлом

### Опис

```methodsynopsis
public DOMNode::insertBefore(DOMNode $node, ?DOMNode $child = null): DOMNode|false
```

Ця функція вставляє новий вузол перед вказаним вузлом. Щоб вносити зміни в доданий дочірній вузол, необхідно використовувати вузол, що повертається.

При використанні існуючого вузла його буде переміщено.

### Список параметрів

`node`

Новий вузол.

`child`

Контрольний вузол. Якщо відсутня, то `node` додається до кінця списку нащадків.

### Значення, що повертаються

Повертає доданий вузол або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний тільки для читання або попередній батько вузла, що вставляється, доступний тільки для читання.

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип вузла не підтримує нащадків типу, що має вузол `node`або якщо доданий вузол є предком цільового вузла або ним самим.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо `node` створено іншому документі, відмінному від цього, у якому було створено цей вузол.

**`DOM_NOT_FOUND`**

Виникає, якщо `child`не является дочерним узлом данного узла.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
