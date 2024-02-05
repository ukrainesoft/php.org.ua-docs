---
navigation:
  - domchildnode.after.md: '« DOMChildNode::after'
  - domchildnode.remove.md: 'DOMChildNode::remove »'
  - index.md: PHP Manual
  - class.domchildnode.md: DOMChildNode
title: 'DOMChildNode::before'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMChildNode::before

(PHP 8)

DOMChildNode::before — Додає вузли перед вузлом.

### Опис

```methodsynopsis
public DOMChildNode::before(DOMNode|string ...$nodes): void
```

Додає передані `nodes`перед узлом.

### Список параметрів

`nodes`

Вузли, які потрібно додати перед вузлом. Рядки автоматично перетворюються на текстові вузли.

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

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) \- Додає вузли після вузла
-   [DOMChildNode::remove()](domchildnode.remove.md) \- видаляє вузол
-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) \- Замінює вузол на нові вузли
