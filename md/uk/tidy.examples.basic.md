---
navigation:
  - tidy.examples.md: « Приклади
  - class.tidy.md: tidy »
  - index.md: PHP Manual
  - tidy.examples.md: Приклади
title: Приклад використання Tidy
---
## Приклад використання Tidy

Простий приклад демонструє базові можливості використання Tidy.

**Приклад #1 Базові можливості використання Tidy**

```php
<?php
ob_start();
?>
<html>a html document</html>
<?php
$html = ob_get_clean();

// Установка конфигурации
$config = array(
           'indent'         => true,
           'output-xhtml'   => true,
           'wrap'           => 200);

// Tidy
$tidy = new tidy;
$tidy->parseString($html, $config, 'utf8');
$tidy->cleanRepair();

// Вывод
echo $tidy;
?>
```
