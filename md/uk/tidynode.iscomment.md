---
navigation:
  - tidynode.isasp.md: '« tidyNode::isAsp'
  - tidynode.ishtml.md: 'tidyNode::isHtml »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::isComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Приклад #1 Вилучення коментарів із змішаного HTML-документа**

```php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>заголовок</title>'; ?>
<#
  /* JSTE код */
  alert('Привет Мир');
#>
</head>
<body>

<?php
  // PHP-код
  echo 'привет мир!';
?>

<%
  /* ASP код */
  response.write("Привет Мир!")
%>

<!-- Комментарии -->
Привет Мир
</body></html>
За пределами HTML кода
HTML;


$tidy = tidy_parse_string($html);
$num = 0;

get_nodes($tidy->html());

function get_nodes($node) {

    // проверяет текущий узел на соответствие требуемому типу
    if($node->isComment()) {
        echo "\n\n# узел комментария #" . ++$GLOBALS['num'] . "\n";
        echo $node->value;
    }

    // проверяет существование потомков у текущего узла
    if($node->hasChildren()) {
        foreach($node->child as $child) {
            get_nodes($child);
        }
    }
}

?>
```

Результат виконання наведеного прикладу:

```
# узел комментария #1
<!-- Комментарии -->
```
