---
navigation:
  - domparentnode.append.md: '« DOMParentNode::append'
  - domparentnode.replacechildren.md: 'DOMParentNode::replaceChildren »'
  - index.md: PHP Manual
  - class.domparentnode.md: DOMParentNode
title: 'DOMParentNode::prepend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMParentNode::prepend

(PHP 8)

DOMParentNode::prepend — Додає вузли перед першим дочірнім вузлом

### Опис

```methodsynopsis
public DOMParentNode::prepend(DOMNode|string ...$nodes): void
```

Додає один чи кілька `nodes` до списку дочірніх вузлів перед першим дочірнім вузлом.

### Список параметрів

`nodes`

Вузли, які потрібно додати. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик цього методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Дивіться також

-   [DOMParentNode::append()](domparentnode.append.md) \- Додає вузли після останнього дочірнього вузла
