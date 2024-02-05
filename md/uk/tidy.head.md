---
navigation:
  - tidy.getstatus.md: '« tidy::getStatus'
  - tidy.md.md: 'tidy::html »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::head'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::head

# tidy\_get\_head

(PHP 5, PHP 7, PHP 8, PECL tidy 0.5.2-1.0.0)

tidy::head -- tidy\_get\_head — Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега разобранного tidy-дерева

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::head(): ?tidyNode
```

Процедурний стиль

```methodsynopsis
tidy_get_head(tidy $tidy): ?tidyNode
```

Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега разобранного tidy-дерева.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.md)

### Приклади

**Приклад #1 Приклад використання** tidy::head()\*\*\*\*

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

$head = $tidy->head();
echo $head->value;
?>
```

Результат виконання наведеного прикладу:

```
<head>
<title>тест</title>
</head>
```

### Дивіться також

-   [tidy::body()](tidy.body.md) \- Повертає об'єкт tidyNode, починаючи з тегаразобранного tidy-дерева
-   [tidy::html()](tidy.md.md) \- Повертає об'єкт tidyNode, починаючи з тегаразобранного tidy-дерева
