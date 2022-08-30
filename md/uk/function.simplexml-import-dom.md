Отримує об'єкт класу SimpleXMLElement із вузла DOM

-   [« Функции SimpleXML](ref.simplexml.html)
    
-   [simplexmlloadfile »](function.simplexml-load-file.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SimpleXML](ref.simplexml.html)
    
-   Отримує об'єкт класу SimpleXMLElement із вузла DOM
    

# simplexmlimportdom

(PHP 5, PHP 7, PHP 8)

simplexmlimportdom — Отримує об'єкт класу `SimpleXMLElement` з вузла DOM

### Опис

```methodsynopsis
simplexml_import_dom(SimpleXMLElement|DOMNode $node, ?string $class_name = SimpleXMLElement::class): ?SimpleXMLElement
```

Ця функція бере вузол документа [DOM](book.dom.html) і перетворює його на вузол SimpleXML. Потім цей новий об'єкт можна використовувати як первинний елемент SimpleXML.

### Список параметрів

`node`

Вузол-елемент [DOM](book.dom.html)

`class_name`

Ви можете використовувати цей додатковий параметр, щоб функція **simplexmlimportdom()** повертала об'єкт вказаного класу. Цей клас має розширювати клас [SimpleXMLElement](class.simplexmlelement.html)

### Значення, що повертаються

Повертає [SimpleXMLElement](class.simplexmlelement.html) або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Імпорт DOM**

```php
<?php
$dom = new DOMDocument;
$dom->loadXML('<books><book><title>чепуха</title></book></books>');
if (!$dom) {
    echo 'Ошибка при разборе документа';
    exit;
}

$s = simplexml_import_dom($dom);

echo $s->book[0]->title;
?>
```

Результат виконання цього прикладу:

```
чепуха
```

### Дивіться також

-   [domimportsimplexml()](function.dom-import-simplexml.html) - Отримує об'єкт класу DOMElement із об'єкта класу SimpleXMLElement
-   [Базовое использование SimpleXML](simplexml.examples-basic.html)