---
navigation:
  - class.domdocument.md: « DOMDocument
  - domdocument.append.md: 'DOMDocument::append »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::adoptNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::adoptNode

(PHP >= 8.3)

DOMDocument::adoptNode — Переносить вузол з іншого документа

### Опис

```methodsynopsis
public DOMDocument::adoptNode(DOMNode $node): DOMNode|false
```

Переносить вузол іншого документа до поточного документа.

### Список параметрів

`node`

Вузол для перенесення.

### Значення, що повертаються

Повертає вузол, який був перенесений або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NOT_SUPPORTED_ERR`**

Виникає, якщо тип вузла не підтримується для перенесення документів.

### Приклади

**Пример #1 Пример использования метода**DOMDocument::adoptNode()\*\*\*\*

Перенесення елемента hello з першого документа до другого.

```php
<?php
$doc1 = new DOMDocument;
$doc1->loadXML("<container><hello><world/></hello></container>");
$hello = $doc1->documentElement->firstChild;

$doc2 = new DOMDocument;
$doc2->loadXML("<root/>");
$doc2->documentElement->appendChild($doc2->adoptNode($hello));

echo $doc1->saveXML() . PHP_EOL;
echo $doc2->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container/>

<?xml version="1.0"?>
<root><hello><world/></hello></root>
```

### Дивіться також

-   [DOMDocument::importNode()](domdocument.importnode.md) \- Імпортувати вузол у поточний документ
