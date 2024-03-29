---
navigation:
  - tidynode.construct.md: '« tidyNode::\_\_construct'
  - tidynode.haschildren.md: 'tidyNode::hasChildren »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::getParent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidyNode::getParent

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

tidyNode::getParent — Повертає батьківський вузол поточного вузла

### Опис

```methodsynopsis
public tidyNode::getParent(): ?tidyNode
```

Повертає вузол поточного вузла.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.md)якщо вузол має батька, в іншому випадку повертає **`null`**

### Приклади

**Приклад #1 Приклад використання функції** tidyNode::getParent()\*\*\*\*

```php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>заголовок</title>'; ?>
<#
  /* JSTE-код */
  alert('Hello World');
#>
 </head>
 <body>
 Hello World
 </body>
</html>

HTML;


$tidy = tidy_parse_string($html);
$num = 0;

$node = $tidy->html()->child[0]->child[0];

var_dump($node->getparent()->name);
?>
```

Результат виконання наведеного прикладу:

```
string(4) "head"
```
