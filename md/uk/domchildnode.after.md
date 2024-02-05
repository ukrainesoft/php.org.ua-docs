---
navigation:
  - class.domchildnode.md: « DOMChildNode
  - domchildnode.before.md: 'DOMChildNode::before »'
  - index.md: PHP Manual
  - class.domchildnode.md: DOMChildNode
title: 'DOMChildNode::after'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMChildNode::after

(PHP 8)

DOMChildNode::after — Додає вузли після вузла

### Опис

```methodsynopsis
public DOMChildNode::after(DOMNode|string ...$nodes): void
```

Додає передані `nodes`после узла.

### Список параметрів

`nodes`

Вузли, які потрібно додати після вузла. Рядки автоматично перетворюються на текстові вузли.

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
| 8.3.0 | Виклик цього методу на вузлі, у якого немає батьківського вузла, тепер нічого не робить, щоб привести поведінку у відповідність до специфікації DOM. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |
| 8.3.0 | Виклик цього методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Дивіться також

-   [DOMChildNode::before()](domchildnode.before.md) \- Додає вузли перед вузлом
-   [DOMChildNode::remove()](domchildnode.remove.md) \- видаляє вузол
-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) \- Замінює вузол на нові вузли
-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
