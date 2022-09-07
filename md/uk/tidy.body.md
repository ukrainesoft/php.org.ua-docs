---
navigation:
  - class.tidy.md: « tidy
  - tidy.cleanrepair.md: 'tidy::cleanRepair »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::body'
---
# tidy::body

# tidygetbody

(PHP 5, PHP 7, PHP 8, PECL tidy 0.5.2-1.0)

tidy::body -- tidygetbody — Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега розібраного tidy-дерева

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::body(): ?tidyNode
```

Процедурний стиль

```methodsynopsis
tidy_get_body(tidy $tidy): ?tidyNode
```

Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега розібраного tidy-дерева.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега розібраного tidy-дерева.

### Приклади

**Приклад #1 Приклад використання **tidy::getBody()****

```php
<?php
$html = '
<html>
  <head>
    <title>тест</title>
  </head>
  <body>
    <p>параграф</p>
  </body>
</html>';

$tidy = tidy_parse_string($html);

$body = $tidy->Body();
echo $body->value;
?>
```

Результат виконання цього прикладу:

```
<body>
<p>параграф</p>
</body>
```

### Дивіться також

-   [tidy::head()](tidy.head.md) - Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
-   [tidy::html()](tidy.html.md) - Повертає об'єкт tidyNode, починаючи з тега розібраного tidy-дерева
