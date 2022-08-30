Імпортувати вузол у поточний документ

-   [« DOMDocument::getElementsByTagNameNS](domdocument.getelementsbytagnamens.html)
    
-   [DOMDocument::load »](domdocument.load.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Імпортувати вузол у поточний документ
    

# DOMDocument::importNode

(PHP 5, PHP 7, PHP 8)

DOMDocument::importNode — Імпортувати вузол у поточний документ

### Опис

```methodsynopsis
public DOMDocument::importNode(DOMNode $node, bool $deep = false): DOMNode|false
```

Ця функція повертає копію імпортованого вузла та пов'язує її з поточним документом.

### Список параметрів

`node`

Вузол для імпорту.

`deep`

Якщо встановлено значення **`true`**, цей метод буде рекурсивно імпортувати піддерево вузла `node`

> **Зауваження**
> 
> Щоб скопіювалися атрибути вузла, `deep` повинен бути встановлений у **`true`**

### Значення, що повертаються

Скопійований вузол або \*\*`false`\*\*якщо він не може бути скопійований.

### Помилки

Якщо вузол не може бути імпортований, буде викинуто виняток [DOMException](class.domexception.html)

### Приклади

**Приклад #1 Приклад використання **DOMDocument::importNode()****

Копіювання вузлів між документами.

```php
<?php

$orgdoc = new DOMDocument;
$orgdoc->loadXML("<root><element><child>text in child</child></element></root>");

// Узел, который будет импортирован в новый документ
$node = $orgdoc->getElementsByTagName("element")->item(0);


// Создание нового документа
$newdoc = new DOMDocument;
$newdoc->formatOutput = true;

// Добавление разметки
$newdoc->loadXML("<root><someelement>text in some element</someelement></root>");

echo "Новый документ перед добавлением в него узлов:\n";
echo $newdoc->saveXML();

// Импорт узла и всех его потомков в документ
$node = $newdoc->importNode($node, true);
// И затем добавление его в корневой узел
$newdoc->documentElement->appendChild($node);

echo "\nНовый документ после добавления в него узлов:\n";
echo $newdoc->saveXML();
?>
```

Результат виконання цього прикладу:

```
Новый документ перед добавлением в него узлов:
<?xml version="1.0"?>
<root>
  <someelement>text in some element</someelement>
</root>

Новый документ после добавления в него узлов:
<?xml version="1.0"?>
<root>
  <someelement>text in some element</someelement>
  <element>
    <child>text in child</child>
  </element>
</root>
```