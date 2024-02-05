---
navigation:
  - domelement.setidattributens.md: '« DOMElement::setIdAttributeNS'
  - class.domentity.md: DOMEntity »
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::toggleAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::toggleAttribute

(PHP 8 >= 8.3.0)

DOMElement::toggleAttribute — Перемикає атрибут

### Опис

```methodsynopsis
public DOMElement::toggleAttribute(string $qualifiedName, ?bool $force = null): bool
```

Перемикає атрибут.

### Список параметрів

`qualifiedName`

Кваліфіковане ім'я атрибуту.

`force`

-   якщо **`null`**, метод перемикає атрибут.
-   якщо **`true`**, метод додасть атрибут
-   якщо **`false`**, метод видалить атрибут

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо атрибут присутній після завершення виклику, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::toggleAttribute()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML("<?xml version='1.0'?><container selected=\"\"/>");

var_dump($dom->documentElement->toggleAttribute('selected'));
echo $dom->saveXML() . PHP_EOL;

var_dump($dom->documentElement->toggleAttribute('selected'));
echo $dom->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
<?xml version="1.0"?>
<container/>

bool(true)
<?xml version="1.0"?>
<container selected=""/>
```
