---
navigation:
  - tidynode.haschildren.md: '« tidyNode::hasChildren'
  - tidynode.isasp.md: 'tidyNode::isAsp »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::hasSiblings'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

**Пример #1 Пример использования функции**tidyNode::hasSiblings()\*\*\*\*

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

// тег html
var_dump($tidy->html()->hasSiblings());

// тег head
var_dump($tidy->html()->child[0]->hasSiblings());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```
