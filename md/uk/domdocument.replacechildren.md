---
navigation:
  - domdocument.relaxngvalidatesource.md: '« DOMDocument::relaxNGValidateSource'
  - domdocument.save.md: 'DOMDocument::save »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::replaceChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::replaceChildren

(PHP 8 >= 8.3.0)

DOMDocument::replaceChildren — Замінює дочірні вузли в документі

### Опис

```methodsynopsis
public DOMDocument::replaceChildren(DOMNode|string ...$nodes): void
```

Замінює дочірні вузли у документі новими вузлами `nodes`

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

**Пример #1 Пример использования метода**DOMDocument::replaceChildren()\*\*\*\*

Заміна дочірніх вузлів у документі новими вузлами.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><hello/></container>");

$doc->replaceWith("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
beautiful
<world/>
```

### Дивіться також

-   [DOMParentNode::replaceChildren()](domparentnode.replacechildren.md) \- Замінює нащадків у вузлі
-   [DOMDocument::append()](domdocument.append.md) \- Додає вузли після останнього дочірнього вузла
-   [DOMDocument::prepend()](domdocument.prepend.md) \- додає вузли перед першим дочірнім вузлом
