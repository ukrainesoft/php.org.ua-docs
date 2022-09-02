---
navigation:
  - domtext.iselementcontentwhitespace.md: '« DOMText::isElementContentWhitespace'
  - domtext.splittext.md: 'DOMText::splitText »'
  - index.md: PHP Manual
  - class.domtext.md: DOMText
title: 'DOMText::isWhitespaceInElementContent'
---
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
