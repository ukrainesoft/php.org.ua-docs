---
navigation:
  - domelement.hasattributens.md: '« DOMElement::hasAttributeNS'
  - domelement.insertadjacenttext.md: 'DOMElement::insertAdjacentText »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::insertAdjacentElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::insertAdjacentElement

(PHP 8 >= 8.3.0)

DOMElement::insertAdjacentElement — Додає сусідній елемент

### Опис

```methodsynopsis
public DOMElement::insertAdjacentElement(string $where, DOMElement $element): ?DOMElement
```

Додає елемент у відносну позицію, задану параметром `where`

### Список параметрів

`where`

-   `beforebegin`\- Додавання перед цільовим елементом.
-   `afterbegin`\- Додавання першого дочірнього елемента цільового елемента.
-   `beforeend`\- Додавання як останній дочірній елемент цільового елемента.
-   `afterend`\- Додавання після цільового елемента.

`element`

Елемент додавання.

### Значення, що повертаються

Повертає [DOMElement](class.domelement.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования метода**DOMElement::insertAdjacentElement()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML('<?xml version="1.0"?><container><p>foo</p></container>');
$container = $dom->documentElement;
$p = $container->firstElementChild;

$p->insertAdjacentElement('beforebegin', $dom->createElement('A'));
echo $dom->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container><A/><p>foo</p></container>
```

### Дивіться також

-   [DOMElement::insertAdjacentText()](domelement.insertadjacenttext.md) \- Додає сусідній текст
