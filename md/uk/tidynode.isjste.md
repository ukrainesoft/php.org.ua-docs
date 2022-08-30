Перевіряє поточний вузол на відповідність JSTE

-   [« tidyNode::isHtml](tidynode.ishtml.md)
    
-   [tidyNode::isPhp »](tidynode.isphp.md)
    
-   [PHP Manual](index.md)
    
-   [tidyNode](class.tidynode.md)
    
-   Перевіряє поточний вузол на відповідність JSTE
    

# tidyNode::isJste

(PHP 5, PHP 7, PHP 8)

tidyNode::isJste — Перевіряє поточний вузол на відповідність JSTE

### Опис

```methodsynopsis
public tidyNode::isJste(): bool
```

Повідомляє, якщо вузол відповідає JSTE.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо вузол є JSTE, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Вилучення JSTE-коду із змішаного HTML-документа**

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
    if($node->isJste()) {
        echo "\n\n# jste-узел #" . ++$GLOBALS['num'] . "\n";
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
# jste-узел #1
<#
  /* JSTE-код */
  alert('Привет Мир');
#>
```