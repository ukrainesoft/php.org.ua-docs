---
navigation:
  - tidynode.isasp.html: '« tidyNode::isAsp'
  - tidynode.ishtml.html: 'tidyNode::isHtml »'
  - index.html: PHP Manual
  - class.tidynode.html: tidyNode
title: 'tidyNode::isComment'
---
# tidyNode::isComment

(PHP 5, PHP 7, PHP 8)

tidyNode::isComment — Перевіряє, чи є вузол коментарем

### Опис

```methodsynopsis
public tidyNode::isComment(): bool
```

Перевіряє, чи є вузол коментарем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо вузол є коментарем, інакше повертає **`false`**

### Приклади

**Приклад #1 Вилучення коментарів із змішаного HTML-документу**

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
    if($node->isComment()) {
        echo "\n\n# узел комментария #" . ++$GLOBALS['num'] . "\n";
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
# узел комментария #1
<!-- Комментарии -->
```
