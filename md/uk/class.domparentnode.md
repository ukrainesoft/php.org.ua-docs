---
navigation:
  - class.domnotation.md: « DOMNotation
  - domparentnode.append.md: 'DOMParentNode::append »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Інтерфейс DOMParentNode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс DOMParentNode

(PHP 8)

## Огляд інтерфейсів

```classsynopsis

    
     interface DOMParentNode {

    /* Методы */
    
   public append(DOMNode|string ...$nodes): void
public prepend(DOMNode|string ...$nodes): void
public replaceChildren(DOMNode|string ...$nodes): void

   }
```

## Зміст

-   [DOMParentNode::append](domparentnode.append.md)— Додає вузли після останнього дочірнього вузла
-   [DOMParentNode::prepend](domparentnode.prepend.md) \- Додає вузли перед першим дочірнім вузлом
-   [DOMParentNode::replaceChildren](domparentnode.replacechildren.md)— Замінює нащадків у вузлі
