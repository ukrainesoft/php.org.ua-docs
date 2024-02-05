---
navigation:
  - domnode.removechild.md: '« DOMNode::removeChild'
  - class.domnodelist.md: DOMNodeList »
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::replaceChild'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::replaceChild

(PHP 5, PHP 7, PHP 8)

DOMNode::replaceChild — Замінює дочірній вузол

### Опис

```methodsynopsis
public DOMNode::replaceChild(DOMNode $node, DOMNode $child): DOMNode|false
```

Функция заменяет дочерний узел`child` новим вузлом. Якщо вузол `node` вже є дочірнім, то він не буде доданий вдруге. Якщо заміна пройшла успішно, то буде повернуто старий (замінний) вузол.

### Список параметрів

`node`

Новий вузол. Повинен бути частиною цільового документа, тобто створений за допомогою одного з методів DOMDocument->createXXX() або імпортований у документ через [DOMDocument::importNode](domdocument.importnode.md)

`child`

Старий вузол.

### Значення, що повертаються

Старий вузол або \*\*`false`\*\*в случае возникновения ошибки.

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

-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) \- Замінює вузол на нові вузли
-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMNode::removeChild()](domnode.removechild.md) \- видаляє дочірній вузол зі списку нащадків
