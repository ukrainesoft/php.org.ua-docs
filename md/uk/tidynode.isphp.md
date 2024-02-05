---
navigation:
  - tidynode.isjste.md: '« tidyNode::isJste'
  - tidynode.istext.md: 'tidyNode::isText »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::isPhp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidyNode::isPhp

(PHP 5, PHP 7, PHP 8)

tidyNode::isPhp — Перевіряє, чи є поточний вузол PHP-кодом

### Опис

```methodsynopsis
public tidyNode::isPhp(): bool
```

Перевіряє, чи є поточний вузол PHP-кодом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо вузол є PHP-кодом, інакше повертає **`false`**

### Приклади

**Приклад #1 Вилучення PHP-коду із змішаного HTML-документа**

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
    if($node->isPhp()) {
        echo "\n\n# php-узел #" . ++$GLOBALS['num'] . "\n";
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
# php-узел #1
<?php echo '<title>заголовок</title>'; ?>

# php-узел #2
<?php
  // PHP-код
  echo 'привет мир!';
?>
```
