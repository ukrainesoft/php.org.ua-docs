---
navigation:
  - ref.simplexml.md: « Функції SimpleXML
  - function.simplexml-load-file.md: simplexml\_load\_file »
  - index.md: PHP Manual
  - ref.simplexml.md: Функції SimpleXML
title: simplexml\_import\_dom
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# simplexml\_import\_dom

(PHP 5, PHP 7, PHP 8)

simplexml\_import\_dom — Отримує об'єкт класу `SimpleXMLElement`из узла DOM

### Опис

```methodsynopsis
simplexml_import_dom(SimpleXMLElement|DOMNode $node, ?string $class_name = SimpleXMLElement::class): ?SimpleXMLElement
```

Ця функція бере вузол документа [DOM](book.dom.md) і перетворює його на вузол SimpleXML. Потім цей новий об'єкт можна використовувати як первинний елемент SimpleXML.

### Список параметрів

`node`

Вузол-елемент [DOM](book.dom.md)

`class_name`

Ви можете використовувати цей додатковий параметр, щоб функція **simplexml\_import\_dom()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.md)

### Значення, що повертаються

Повертає [SimpleXMLElement](class.simplexmlelement.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Імпорт DOM**

```php
<?php
$dom = new DOMDocument;
$dom->loadXML('<books><book><title>чепуха</title></book></books>');
if (!$dom) {
    echo 'Ошибка при разборе документа';
    exit;
}

$s = simplexml_import_dom($dom);

echo $s->book[0]->title;
?>
```

Результат виконання наведеного прикладу:

```
чепуха
```

### Дивіться також

-   [dom\_import\_simplexml()](function.dom-import-simplexml.md) \- Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement
-   [Базове використання SimpleXML](simplexml.examples-basic.md)
