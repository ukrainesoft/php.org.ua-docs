---
navigation:
  - domelement.insertadjacentelement.md: '« DOMElement::insertAdjacentElement'
  - domelement.prepend.md: 'DOMElement::prepend »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::insertAdjacentText'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::insertAdjacentText

(PHP 8 >= 8.3.0)

DOMElement::insertAdjacentText — Додає сусідній текст

### Опис

```methodsynopsis
public DOMElement::insertAdjacentText(string $where, string $data): void
```

Додає текст у відносну позицію, задану параметром `where`

### Список параметрів

`where`

-   `beforebegin`\- Додавання перед цільовим елементом.
-   `afterbegin`\- Додавання першого дочірнього елемента цільового елемента.
-   `beforeend`\- Додавання як останній дочірній елемент цільового елемента.
-   `afterend`\- Додавання після цільового елемента.

`data`

Рядок для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::insertAdjacentText()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML('<?xml version="1.0"?><container><p>H</p></container>');

$container = $dom->documentElement;
$p = $container->firstElementChild;

$p->insertAdjacentText("afterbegin", "P");
$p->insertAdjacentText("beforeend", "P");

echo $dom->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container><p>PHP</p></container>
```

### Дивіться також

-   [DOMElement::insertAdjacentElement()](domelement.insertadjacentelement.md) \- Додає сусідній елемент
