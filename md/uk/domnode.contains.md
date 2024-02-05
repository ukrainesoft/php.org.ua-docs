---
navigation:
  - domnode.clonenode.md: '« DOMNode::cloneNode'
  - domnode.getlineno.md: 'DOMNode::getLineNo »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::contains

(PHP 8 >= 8.3.0)

DOMNode::contains — Перевіряє, чи містить вузол інший вузол

### Опис

```methodsynopsis
public DOMNode::contains(DOMNode|DOMNameSpaceNode|null $other): bool
```

Перевіряє, чи містить вузол інший вузол - передано в параметр `other`

### Список параметрів

`other`

Вузол, який потрібно перевірити.

### Значення, що повертаються

Повертає **`true`**якщо вузол містить вузол, заданий параметром `other`, иначе**`false`**

### Приклади

**Пример #1 Пример использования метода**DOMNode::contains()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML(<<<XML
<!DOCTYPE HTML>
<html>
   <body>
       <main>
           <p>Привет, мир!</p>
       </main>
   </body>
</html>
XML);

$xpath = new DOMXPath($dom);
$main = $xpath->query("//main")[0];

var_dump($dom->documentElement->contains($main));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
