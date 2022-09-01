---
navigation:
  - tidy.repairstring.md: '« tidy::repairString'
  - class.tidynode.md: tidyNode »
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::root'
---
# tidy::root

# tidygetroot

(PHP 5, PHP 7, PHP 8, PECL tidy 0.5.2-1.0.0)

tidy::root -- tidygetroot — Повертає об'єкт [tidyNode](class.tidynode.md), що представляє вершину розібраного tidy-дерева

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::root(): ?tidyNode
```

Процедурний стиль

```methodsynopsis
tidy_get_root(tidy $tidy): ?tidyNode
```

Повертає об'єкт [tidyNode](class.tidynode.md), що представляє вершину розібраного tidy-дерева.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.md)

### Приклади

**Приклад #1 Приклад використання **tidy::root()****

```php
<?php

$html = <<< HTML
<html><body>

<p>параграф</p>
<br/>

</body></html>
HTML;

$tidy = tidy_parse_string($html);
dump_nodes($tidy->root(), 1);


function dump_nodes($node, $indent) {

    if($node->hasChildren()) {
        foreach($node->child as $child) {
            echo str_repeat('.', $indent*2) . ($child->name ? $child->name : '"'.$child->value.'"'). "\n";

            dump_nodes($child, $indent+1);
        }
    }
}
?>
```

Результат виконання цього прикладу:

```
..html
....head
......title
....body
......p
........"параграф"
......br
```
