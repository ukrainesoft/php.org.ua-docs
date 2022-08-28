Інтерфейс DOMChildNode

-   [« DOMCharacterData::substringData](domcharacterdata.substringdata.html)
    
-   [DOMChildNode::after »](domchildnode.after.html)
    
-   [PHP Manual](index.html)
    
-   [DOM](book.dom.html)
    
-   Інтерфейс DOMChildNode
    

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

-   [DOMChildNode::after](domchildnode.after.html) - Додає вузли після вузла
-   [DOMChildNode::before](domchildnode.before.html) - Додає вузли перед вузлом
-   [DOMChildNode::remove](domchildnode.remove.html) - Видаляє вузол
-   [DOMChildNode::replaceWith](domchildnode.replacewith.html) - Замінює вузол новими вузлами