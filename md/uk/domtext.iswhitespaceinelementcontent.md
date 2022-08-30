Визначає, чи містить текстовий вузол пробіли у вмісті

-   [« DOMText::isElementContentWhitespace](domtext.iselementcontentwhitespace.html)
    
-   [DOMText::splitText »](domtext.splittext.html)
    
-   [PHP Manual](index.html)
    
-   [DOMText](class.domtext.html)
    
-   Визначає, чи містить текстовий вузол пробіли у вмісті
    

# DOMText::isWhitespaceInElementContent

(PHP 5, PHP 7, PHP 8)

DOMText::isWhitespaceInElementContent — Визначає, чи містить текстовий вузол пробіли у вмісті

### Опис

```methodsynopsis
public DOMText::isWhitespaceInElementContent(): bool
```

Визначає, чи є пробіли у вмісті текстового вузла, чи він порожній. Текстові вузли можуть містити пробіли у вмісті під час завантаження документа.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо вузол складається тільки з нуля або більше пробілів. Повертає **`false`** в іншому випадку.