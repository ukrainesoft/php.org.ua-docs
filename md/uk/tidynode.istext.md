---
navigation:
  - tidynode.isphp.md: '« tidyNode::isPhp'
  - ref.tidy.md: Tidy »
  - index.md: PHP Manual
  - class.tidynode.md: tidyNode
title: 'tidyNode::isText'
---
# tidyNode::isText

(PHP 5, PHP 7, PHP 8)

tidyNode::isText — Перевіряє, чи поточний вузол є звичайним текстом (не розміткою)

### Опис

```methodsynopsis
public tidyNode::isText(): bool
```

Перевіряє, чи поточний вузол є звичайним текстом (без будь-якої розмітки).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо вузол є текст, в іншому випадку повертає **`false`**

### Приклади

**Приклад #1 Вилучення звичайного тексту із змішаного HTML-документа**

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
    if($node->isText()) {
        echo "\n\n# текстовый узел #" . ++$GLOBALS['num'] . "\n";
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

Результат виконання цього прикладу:

```
# текстовый узел #1
Привет Мир

# текстовый узел #2
За пределами HTML кода
```
