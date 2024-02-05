---
navigation:
  - tidy.head.md: '« tidy::head'
  - tidy.isxhtml.md: 'tidy::isXhtml »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::html'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::html

# tidy\_get\_html

(PHP 5, PHP 7, PHP 8, PECL tidy 0.5.2-1.0.0)

tidy::html -- tidy\_get\_html — Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега разобранного tidy-дерева

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::html(): ?tidyNode
```

Процедурний стиль

```methodsynopsis
tidy_get_html(tidy $tidy): ?tidyNode
```

Повертає об'єкт [tidyNode](class.tidynode.md), починаючи з тега разобранного tidy-дерева.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає об'єкт [tidyNode](class.tidynode.md)

### Приклади

**Приклад #1 Приклад використання** tidy::html()\*\*\*\*

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

$html = $tidy->html();
echo $html->value;
?>
```

Результат виконання наведеного прикладу:

```
<html>
<head>
<title>тест</title>
</head>
<body>
<p>параграф</p>
</body>
</html>
```

### Дивіться також

-   [tidy::body()](tidy.body.md) \- Повертає об'єкт tidyNode, починаючи з тегаразобранного tidy-дерева
-   [tidy::head()](tidy.head.md) \- Повертає об'єкт tidyNode, починаючи з тегаразобранного tidy-дерева
