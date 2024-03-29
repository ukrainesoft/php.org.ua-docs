---
navigation:
  - tidynode.iscomment.md: '« tidyNode::isComment'
  - tidynode.isjste.md: 'tidyNode::isJste »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::isHtml'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidyNode::isHtml

(PHP 5, PHP 7, PHP 8)

tidyNode::isHtml — Перевіряє, чи є вузол вузлом елемента

### Опис

```methodsynopsis
public tidyNode::isHtml(): bool
```

Перевіряє, чи є вузол вузлом елемента, але з кореневим вузлом документа.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо вузол є вузлом елемента, але не кореневим вузлом документа, в іншому випадку повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.24, 7.4.12 | Виправлено, тепер функція поводиться розумно. Раніше майже будь-який вузол вважався вузлом HTML. |

### Приклади

**Приклад #1 Вилучення HTML-коду із змішаного HTML-документа**

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
    if($node->isHtml()) {
        echo "\n\n# html нода #" . ++$GLOBALS['num'] . "\n";
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
# html узел #1
<html>
<head>
<?php echo '<title>заголовок</title>'; ?><#
  /* JSTE код */
  alert('Привет Мир');
#>
<title></title>
</head>
<body>
<?php
  // PHP-код
  echo 'привет мир!';
?><%
  /* ASP код */
  response.write("Привет Мир!")
%><!-- Комментарии -->
Привет МирЗа пределами HTML кода
</body>
</html>

# html узел #2
<head>
<?php echo '<title>заголовок</title>'; ?><#
  /* JSTE код */
  alert('Привет Мир');
#>
<title></title>
</head>


# html узел #3
<title></title>

# html узел #4
<body>
<?php
  // PHP-код
  echo 'привет мир!';
?><%
  /* ASP код */
  response.write("Привет Мир!")
%><!-- Комментарии -->
Привет МирЗа пределами HTML кода
</body>
```
