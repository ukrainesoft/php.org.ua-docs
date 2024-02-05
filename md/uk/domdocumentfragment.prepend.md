---
navigation:
  - domdocumentfragment.construct.md: '« DOMDocumentFragment::\_\_construct'
  - domdocumentfragment.replacechildren.md: 'DOMDocumentFragment::replaceChildren »'
  - index.md: PHP Manual
  - class.domdocumentfragment.md: DOMDocumentFragment
title: 'DOMDocumentFragment::prepend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocumentFragment::prepend

(PHP 8)

DOMDocumentFragment::prepend — Додає вузли перед першим дочірнім вузлом

### Опис

```methodsynopsis
public DOMDocumentFragment::prepend(DOMNode|string ...$nodes): void
```

Додає один або кілька вузлів `nodes` до списку дочірніх вузлів перед першим дочірнім вузлом.

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

**Приклад #1 Приклад использования метода**DOMDocumentFragment::prepend()\*\*\*\*

Додавання вузлів перед коренем фрагмента.

```php
<?php
$doc = new DOMDocument;
$fragment = $doc->createDocumentFragment();
$fragment->appendChild($doc->createElement("world"));

$fragment->prepend($doc->createElement("hello"), "beautiful");

echo $doc->saveXML($fragment);
?>
```

Результат виконання наведеного прикладу:

```
<hello/>beautiful<world/>
```

### Дивіться також

-   [DOMParentNode::prepend()](domparentnode.prepend.md) \- додає вузли перед першим дочірнім вузлом
-   [DOMDocumentFragment::append()](domdocumentfragment.append.md) \- Додає вузли після останнього дочірнього вузла
