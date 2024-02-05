---
navigation:
  - domdocumentfragment.prepend.md: '« DOMDocumentFragment::prepend'
  - class.domdocumenttype.md: DOMDocumentType »
  - index.md: PHP Manual
  - class.domdocumentfragment.md: DOMDocumentFragment
title: 'DOMDocumentFragment::replaceChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocumentFragment::replaceChildren

(PHP 8 >= 8.3.0)

DOMDocumentFragment::replaceChildren — Замінює дочірні елементи фрагмента

### Опис

```methodsynopsis
public DOMDocumentFragment::replaceChildren(DOMNode|string ...$nodes): void
```

Замінює дочірні елементи фрагмента документа на нові сайти `nodes`

### Список параметрів

`nodes`

Вузли, якими будуть замінені нащадки. Рядки автоматично перетворюються на текстові вузли.

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
| 8.3.0 | Виклик методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Пример #1 Пример использования метода**DOMDocumentFragment::replaceChildren()\*\*\*\*

Заміна дочірніх вузлів на нові.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><hello/></container>");
$fragment = $doc->createDocumentFragment();
$fragment->append("hello");

$fragment->replaceWith("beautiful", $doc->createElement("world"));

echo $doc->saveXML($fragment);
?>
```

Результат виконання наведеного прикладу:

```
beautiful
<world/>
```

### Дивіться також

-   [DOMParentNode::replaceChildren()](domparentnode.replacechildren.md) \- Замінює нащадків у вузлі
-   [DOMDocumentFragment::append()](domdocumentfragment.append.md) \- Додає вузли після останнього дочірнього вузла
-   [DOMDocumentFragment::prepend()](domdocumentfragment.prepend.md) \- додає вузли перед першим дочірнім вузлом
