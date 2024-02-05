---
navigation:
  - tidy.getrelease.md: '« tidy::getRelease'
  - tidy.head.md: 'tidy::head »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::getStatus'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::getStatus

# tidy\_get\_status

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::getStatus -- tidy\_get\_status — Отримує статус зазначеного документа

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::getStatus(): int
```

Процедурний стиль

```methodsynopsis
tidy_get_status(tidy $tidy): int
```

Повертає статус вказаного tidy-об'єкта `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає 0, якщо не було помилок/попереджень, 1 – для попереджень або можливих помилок або 2 – для помилок.

### Приклади

**Пример #1 Пример использования**tidy::getStatus()\*\*\*\*

```php
<?php
$html = '<p>параграф</i>';
$tidy = new tidy();
$tidy->parseString($html);

$tidy2 = new tidy();
$html2 = '<bogus>тест</bogus>';
$tidy2->parseString($html2);

echo $tidy->getStatus(); //1

echo $tidy2->getStatus(); //2
?>
```
