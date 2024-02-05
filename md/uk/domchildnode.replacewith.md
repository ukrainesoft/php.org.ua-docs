---
navigation:
  - domchildnode.remove.md: '« DOMChildNode::remove'
  - class.domcomment.md: DOMComment »
  - index.md: PHP Manual
  - class.domchildnode.md: DOMChildNode
title: 'DOMChildNode::replaceWith'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMChildNode::replaceWith

(PHP 8)

DOMChildNode::replaceWith — Замінює вузол на нові вузли

### Опис

```methodsynopsis
public DOMChildNode::replaceWith(DOMNode|string ...$nodes): void
```

Замінює вузол на нові вузли `nodes`

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

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) \- Додає вузли після вузла
-   [DOMChildNode::before()](domchildnode.before.md) \- Додає вузли перед вузлом
-   [DOMChildNode::remove()](domchildnode.remove.md) \- видаляє вузол
-   [DOMNode::replaceChild()](domnode.replacechild.md) \- Замінює дочірній вузол
