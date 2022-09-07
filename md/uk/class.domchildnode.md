---
navigation:
  - domcharacterdata.substringdata.md: '« DOMCharacterData::substringData'
  - domchildnode.after.md: 'DOMChildNode::after »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Інтерфейс DOMChildNode
---
# Інтерфейс DOMChildNode

(PHP 8)

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface DOMChildNode {

    /* Методы */
    
   public after(DOMNode|string ...$nodes): void
public before(DOMNode|string ...$nodes): void
public remove(): void
public replaceWith(DOMNode|string ...$nodes): void

   }
```

## Зміст

-   [DOMChildNode::after](domchildnode.after.md) - Додає вузли після вузла
-   [DOMChildNode::before](domchildnode.before.md) - Додає вузли перед вузлом
-   [DOMChildNode::remove](domchildnode.remove.md) - Видаляє вузол
-   [DOMChildNode::replaceWith](domchildnode.replacewith.md) - Замінює вузол новими вузлами
