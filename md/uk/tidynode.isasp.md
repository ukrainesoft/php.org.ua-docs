---
navigation:
  - tidynode.hassiblings.md: '« tidyNode::hasSiblings'
  - tidynode.iscomment.md: 'tidyNode::isComment »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::isAsp'
---
# tidyNode::isAsp

(PHP 5, PHP 7, PHP 8)

tidyNode::isAsp — Перевіряє поточний вузол на відповідність ASP

### Опис

```methodsynopsis
public tidyNode::isAsp(): bool
```

Перевіряє поточний вузол на відповідність ASP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо вузол є ASP, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Вилучення коду ASP із змішаного HTML-документа**

```php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>заголовок</title>'; ?>
<#
  /* JSTE код */
  alert('Привет Мир');
#>
</head>
<body>

<?php
  // PHP-код
  echo 'привет мир!';
?>

<%
  /* ASP код */
  response.write("Привет Мир!")
%>

<!-- Комментарии -->
Привет Мир
</body></html>
За пределами HTML кода
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // проверяет текущий узел на соответствие требуемому типу
    if($node->isAsp()) {
        echo "\n\n# asp узел #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // проверяет существование потомков у текущего узла
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

Результат виконання цього прикладу:

```
# asp нода #1
<%
  /* ASP код */
  response.write("Привет Мир!")
%>
```
