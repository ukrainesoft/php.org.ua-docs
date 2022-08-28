Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева

-   [« tidy](class.tidy.html)
    
-   [tidy::cleanRepair »](tidy.cleanrepair.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
    

# tidy::body

# tidygetbody

(PHP 5, PHP 7, PHP 8, PECL tidy 0.5.2-1.0)

tidy::body -- tidygetbody — Повертає об'єкт [tidyNode](class.tidynode.html), починаючи з тега розібраного tidy-дерева

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::body(): ?tidyNode
```

Процедурний стиль

```methodsynopsis
tidy_get_body(tidy $tidy): ?tidyNode
```

Повертає об'єкт [tidyNode](class.tidynode.html), починаючи з тега розібраного tidy-дерева.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.html), починаючи з тега розібраного tidy-дерева.

### Приклади

**Приклад #1 Приклад використання **tidy::getBody()****

```php
<?php
$html = '
<html>
  <head>
    <title>тест</title>
  </head>
  <body>
    <p>параграф</p>
  </body>
</html>';

$tidy = tidy_parse_string($html);

$body = $tidy->Body();
echo $body->value;
?>
```

Результат виконання цього прикладу:

```
<body>
<p>параграф</p>
</body>
```

### Дивіться також

-   [tidy::head()](tidy.head.html) - Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
-   [tidy::html()](tidy.html.html) - Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева