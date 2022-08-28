Отримати номер рядка вузла

-   [« DOMNode::cloneNode](domnode.clonenode.html)
    
-   [DOMNode::getNodePath »](domnode.getnodepath.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNode](class.domnode.html)
    
-   Отримати номер рядка вузла
    

# DOMNode::getLineNo

(PHP 5> = 5.3.0, PHP 7, PHP 8)

DOMNode::getLineNo — Отримати номер рядка вузла

### Опис

```methodsynopsis
public DOMNode::getLineNo(): int
```

Повертає номер рядка, в якому визначено вузол.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Завжди повертає номер рядка, в якому було визначено вузол.

### Приклади

**Приклад #1 Приклад використання **DOMNode::getLineNo()****

```php
<?php
// Определение необходимого для примера XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <node />
</root>
XML;

// Создание нового экземпляра DOMDocument
$dom = new DOMDocument;

// Загрузка XML
$dom->loadXML($xml);

// Вывод номер строки, в которой определён элемент 'node'
printf('Тег <node> определён в строке %d', $dom->getElementsByTagName('node')->item(0)->getLineNo());
?>
```

Результат виконання цього прикладу:

```
Тег <node> определён в строке 3
```