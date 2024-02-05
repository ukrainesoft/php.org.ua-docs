---
navigation:
  - domnode.contains.md: '« DOMNode::contains'
  - domnode.getnodepath.md: 'DOMNode::getNodePath »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::getLineNo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::getLineNo

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

DOMNode::getLineNo — Отримує номер рядка вузла

### Опис

```methodsynopsis
public DOMNode::getLineNo(): int
```

Отримує номер рядка, в якому під час розбирання було визначено вузол.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер рядка, в якому під час аналізу був вузол. Якщо вузол був створений вручну, повернеться

### Приклади

**Приклад #1 Приклад использования метода**DOMNode::getLineNo()\*\*\*\*

```php
<?php
// Определение необходимого для Приклада XML
$xml = <<<XML
<?xml version="1.0" encoding="utf-8"?>
<root>
    <node />
</root>
XML;

// Создание нового экземпляра DOMDocument
$dom = new DOMDocument;

// Загрузка XML
$dom->loadXML($xml);

// Вывод номер строки, в которой определён элемент 'node'
printf('Тег <node> определён в строке %d', $dom->getElementsByTagName('node')->item(0)->getLineNo());
?>
```

Результат виконання наведеного прикладу:

```
Тег <node> определён в строке 3
```
