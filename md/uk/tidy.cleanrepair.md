Виконати налаштоване очищення та відновлення розібраної розмітки

-   [« tidy::body](tidy.body.html)
    
-   [tidy::construct »](tidy.construct.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Виконати налаштоване очищення та відновлення розібраної розмітки
    

# tidy::cleanRepair

# tidycleanrepair

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::cleanRepair -- tidycleanrepair — Виконати налаштоване очищення та відновлення розібраної розмітки

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

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **tidy::cleanrepair()****

```php
<?php
$html = '<p>тест</I>';

$tidy = tidy_parse_string($html);
$tidy->cleanRepair();

echo $tidy;
?>
```

Результат виконання цього прикладу:

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

-   [tidy::repairFile()](tidy.repairfile.html) - Відновлює розмітку файлу та повертає його у вигляді рядка
-   [tidy::repairString()](tidy.repairstring.html) - Відновлює рядок, використовуючи наскільки можна конфігураційний файл