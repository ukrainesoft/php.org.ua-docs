---
navigation:
  - class.domdocumentfragment.md: « DOMDocumentFragment
  - domdocumentfragment.appendxml.md: 'DOMDocumentFragment::appendXML »'
  - index.md: PHP Manual
  - class.domdocumentfragment.md: DOMDocumentFragment
title: 'DOMDocumentFragment::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocumentFragment::append

(PHP 8)

DOMDocumentFragment::append — Додає вузли після останнього дочірнього вузла

### Опис

```methodsynopsis
public DOMDocumentFragment::append(DOMNode|string ...$nodes): void
```

Додає один або кілька вузлів `nodes` до списку дочірніх вузлів після останнього дочірнього вузла.

### Список параметрів

`nodes`

Вузли, які потрібно додати. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик цього методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Пример #1 Пример использования метода**DOMDocumentFragment::append()\*\*\*\*

Додавання вузлів у фрагмент.

```php
<?php
$doc = new DOMDocument;
$fragment = $doc->createDocumentFragment();
$fragment->appendChild($doc->createElement("hello"));

$fragment->append("beautiful", $doc->createElement("world"));

echo $doc->saveXML($fragment);
?>
```

Результат виконання наведеного прикладу:

```
<hello/>beautiful<world/>
```

### Дивіться також

-   [DOMParentNode::append()](domparentnode.append.md) \- Додає вузли після останнього дочірнього вузла
-   [DOMDocumentFragment::prepend()](domdocumentfragment.prepend.md) \- додає вузли перед першим дочірнім вузлом
