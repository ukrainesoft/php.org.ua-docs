---
navigation:
  - splfileobject.fgets.md: '« SplFileObject::fgets'
  - splfileobject.flock.md: 'SplFileObject::flock »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fgetss'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fgetss

(PHP 5 >= 5.1.0, PHP 7)

SplFileObject::fgetss — Отримати рядок із файлу та видалити теги HTML

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public SplFileObject::fgetss(string $allowable_tags = ?): string
```

Робота функції ідентична [SplFileObject::fgets()](splfileobject.fgets.md) за винятком того, що **SplFileObject::fgetss()** намагається очистити рядок від будь-яких тегів HTML та PHP. Function retains the parsing state from call to call, і як це не є equivalent to calling [strip\_tags()](function.strip-tags.md)on the return value of[SplFileObject::fgets()](splfileobject.fgets.md). Функція зберігає стан синтаксичного аналізу від виклику до виклику і тому не еквівалентна виклику [strip\_tags()](function.strip-tags.md) для значення, що повертається [SplFileObject::fgets()](splfileobject.fgets.md)

### Список параметрів

`allowable_tags`

Необов'язковий параметр для вказівки тегів, які не потрібно видаляти.

### Значення, що повертаються

Повертає рядок з файлу, очищений від HTML- та PHP-коду, або \*\*`false`\*\*в случае ошибки.

### Приклади

**Пример #1 Пример использования**SplFileObject::fgetss()\*\*\*\*

```php
<?php
$str = <<<EOD
<html><body>
 <p>Добро пожаловать! Сегодня <?php echo(date('jS')); ?> <?= date('F'); ?>.</p>
</body></html>
Текст вне блока HTML.
EOD;
file_put_contents("sample.php", $str);

$file = new SplFileObject("sample.php");
while (!$file->eof()) {
    echo $file->fgetss();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Добро пожаловать! Сегодня .

Текст вне блока HTML.
```

### Дивіться також

-   [fgetss()](function.fgetss.md) \- Читає рядок з файлу та видаляє HTML-теги
-   [SplFileObject::fgets()](splfileobject.fgets.md) \- Отримує рядок із файлу
-   [SplFileObject::fgetc()](splfileobject.fgetc.md) \- Отримує символ із файлу
-   [SplFileObject::current()](splfileobject.current.md) \- Отримати поточний рядок файлу
-   Фильтр[string.strip\_tags](filters.string.md#filters.string.strip_tags)
