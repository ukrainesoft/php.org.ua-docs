Перевіряє існування сусідніх вузлів

-   [« tidyNode::hasChildren](tidynode.haschildren.html)
    
-   [tidyNode::isAsp »](tidynode.isasp.html)
    
-   [PHP Manual](index.html)
    
-   [tidyNode](class.tidynode.html)
    
-   Перевіряє існування сусідніх вузлів
    

# tidyNode::hasSiblings

(PHP 5, PHP 7, PHP 8)

tidyNode::hasSiblings — Перевіряє існування сусідніх вузлів

### Опис

```methodsynopsis
public tidyNode::hasSiblings(): bool
```

Перевіряє існування сусідніх вузлів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо існують сусідні вузли, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання функції **tidyNode::hasSiblings()****

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

// тег html
var_dump($tidy->html()->hasSiblings());

// тег head
var_dump($tidy->html()->child[0]->hasSiblings());

?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```