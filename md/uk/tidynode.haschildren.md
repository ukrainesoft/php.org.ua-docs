---
navigation:
  - tidynode.getparent.md: '« tidyNode::getParent'
  - tidynode.hassiblings.md: 'tidyNode::hasSiblings »'
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::hasChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidyNode::hasChildren

(PHP 5, PHP 7, PHP 8)

tidyNode::hasChildren — Перевіряє існування нащадків біля вузла

### Опис

```methodsynopsis
public tidyNode::hasChildren(): bool
```

Повідомляє, чи має заданий вузл нащадки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо у вузла є нащадки, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования функции**tidyNode::hasChildren()\*\*\*\*

```php
<?php

$html = <<< HTML
<html><head>
<?php echo '<title>заголовок</title>'; ?>
<#
  /* JSTE-код */
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

// тег head
var_dump($tidy->html()->child[0]->hasChildren());

// php внутри тега head
var_dump($tidy->html()->child[0]->child[0]->hasChildren());

?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```
