---
navigation:
  - tidy.body.md: '« tidy::body'
  - tidy.construct.md: 'tidy::\_\_construct »'
  - index.md: PHP Manual
  - class.tidy.md: tidy
title: 'tidy::cleanRepair'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tidy::cleanRepair

# tidy\_clean\_repair

(PHP 5, PHP 7, PHP 8, PECL tidy >= 0.5.2)

tidy::cleanRepair -- tidy\_clean\_repair — Виконати налаштоване очищення та відновлення розібраної розмітки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::cleanRepair(): bool
```

Процедурний стиль

```methodsynopsis
tidy_clean_repair(tidy $tidy): bool
```

Функція очищує та відновлює отриманий tidy-об'єкт `tidy`

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**tidy::cleanrepair()\*\*\*\*

```php
<?php
$html = '<p>тест</I>';

$tidy = tidy_parse_string($html);
$tidy->cleanRepair();

echo $tidy;
?>
```

Результат виконання наведеного прикладу:

```
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 3.2//EN">
<html>
<head>
<title></title>
</head>
<body>
<p>тест</p>
</body>
</html>
```

### Дивіться також

-   [tidy::repairFile()](tidy.repairfile.md) \- Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairString()](tidy.repairstring.md) \- Відновлює рядок, використовуючи наскільки можна конфігураційний файл
