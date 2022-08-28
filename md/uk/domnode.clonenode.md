Клонує вузол

-   [« DOMNode::C14NFile](domnode.c14nfile.html)
    
-   [DOMNode::getLineNo »](domnode.getlineno.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNode](class.domnode.html)
    
-   Клонує вузол
    

# DOMNode::cloneNode

(PHP 5, PHP 7, PHP 8)

DOMNode::cloneNode — Клонує вузол

### Опис

```methodsynopsis
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
```

Створює копію вузла.

### Список параметрів

`deep`

Вказує, чи потрібно копіювати нащадків. Цей параметр за замовчуванням має значення **`false`**

### Значення, що повертаються

Копія вузла.