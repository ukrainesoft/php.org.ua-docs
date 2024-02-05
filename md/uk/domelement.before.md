---
navigation:
  - domelement.append.md: '« DOMElement::append'
  - domelement.construct.md: 'DOMElement::\_\_construct »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::before'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::before

(PHP 8)

DOMElement::before — Додає вузли перед елементом

### Опис

```methodsynopsis
public DOMElement::before(DOMNode|string ...$nodes): void
```

Додає передані вузли `nodes` перед елементом.

### Список параметрів

`nodes`

Вузли, які потрібно додати перед вузлом. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі батьківського вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик цього методу на вузлі, у якого немає батьківського вузла, тепер нічого не робить, щоб привести поведінку у відповідність до специфікації DOM. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Пример #1 Пример использования метода**DOMElement::before()\*\*\*\*

Додавання вузлів перед елементом "hello".

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<world/>");
$world = $doc->documentElement;

$world->before("hello", $doc->createElement("beautiful"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
hello
<beautiful/>
<world/>
```

### Дивіться також

-   [DOMChildNode::before()](domchildnode.before.md) \- Додає вузли перед вузлом
-   [DOMElement::after()](domelement.after.md) \- Додає вузли після елемента
