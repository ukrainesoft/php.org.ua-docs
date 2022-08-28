Замінює вузол новими вузлами

-   [« DOMChildNode::remove](domchildnode.remove.html)
    
-   [DOMComment »](class.domcomment.html)
    
-   [PHP Manual](index.html)
    
-   [DOMChildNode](class.domchildnode.html)
    
-   Замінює вузол новими вузлами
    

# DOMChildNode::replaceWith

(PHP 8)

DOMChildNode::replaceWith — Замінює вузол новими вузлами

### Опис

```methodsynopsis
public DOMChildNode::replaceWith(DOMNode|string ...$nodes): void
```

Замінює вузол новими переданими `nodes`. Поєднання методу [DOMChildNode::remove()](domchildnode.remove.html) і **DOMChildNode::append()**

### Список параметрів

`nodes`

Вузли, якими потрібно замінити вузол.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.html) - Додає вузли після вузла
-   [DOMChildNode::before()](domchildnode.before.html) - Додає вузли перед вузлом
-   [DOMChildNode::remove()](domchildnode.remove.html) - видаляє вузол
-   [DOMNode::replaceChild()](domnode.replacechild.html) - Замінює дочірній вузол