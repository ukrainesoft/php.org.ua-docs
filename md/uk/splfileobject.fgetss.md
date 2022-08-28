Отримати рядок із файлу та видалити теги HTML

-   [« SplFileObject::fgets](splfileobject.fgets.html)
    
-   [SplFileObject::flock »](splfileobject.flock.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримати рядок із файлу та видалити теги HTML
    

# SplFileObject::fgetss

(PHP 5> = 5.1.0, PHP 7)

SplFileObject::fgetss — Отримати рядок із файлу та видалити теги HTML

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public SplFileObject::fgetss(string $allowable_tags = ?): string
```

Робота функції ідентична [SplFileObject::fgets()](splfileobject.fgets.html) за винятком того, що **SplFileObject::fgetss()** намагається очистити рядок від будь-яких тегів HTML та PHP. Function retains the parsing state from call to call, і як не є подібним до calling [strip\_tags()](function.strip-tags.html) on the return value of [SplFileObject::fgets()](splfileobject.fgets.html). Функція зберігає стан синтаксичного аналізу від виклику до виклику і тому не еквівалентна виклику [strip\_tags()](function.strip-tags.html) для значення, що повертається [SplFileObject::fgets()](splfileobject.fgets.html)

### Список параметрів

`allowable_tags`

Необов'язковий параметр для вказівки тегів, які не потрібно видаляти.

### Значення, що повертаються

Повертає рядок з файлу, очищений від HTML- та PHP-коду, або **`false`** у разі помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fgetss()****

```php
<?php
$str = <<<EOD
<html><body>
 <p>Добро пожаловать! Сегодня <?php echo(date('jS')); ?> <?= date('F'); ?>.</p>
</body></html>
Текст вне блока HTML.
EOD;
file_put_contents("sample.php", $str);

$file = new SplFileObject("sample.php");
while (!$file->eof()) {
    echo $file->fgetss();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Добро пожаловать! Сегодня .

Текст вне блока HTML.
```

### Дивіться також

-   [fgetss()](function.fgetss.html) - Читає рядок з файлу та видаляє HTML-теги
-   [SplFileObject::fgets()](splfileobject.fgets.html) - Отримує рядок із файлу
-   [SplFileObject::fgetc()](splfileobject.fgetc.html) - Отримує символ із файлу
-   [SplFileObject::current()](splfileobject.current.html) - Отримати поточний рядок файлу
-   Фільтр [string.strip\_tags](filters.string.html#filters.string.strip_tags)