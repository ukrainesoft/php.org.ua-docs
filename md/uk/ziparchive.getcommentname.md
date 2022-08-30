Повертає коментар елемента, використовуючи його ім'я

-   [« ZipArchive::getCommentIndex](ziparchive.getcommentindex.md)
    
-   [ZipArchive::getExternalAttributesIndex »](ziparchive.getexternalattributesindex.md)
    
-   [PHP Manual](index.md)
    
-   [ZipArchive](class.ziparchive.md)
    
-   Повертає коментар елемента, використовуючи його ім'я
    

# ZipArchive::getCommentName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::getCommentName — Повертає коментар елемента, використовуючи його ім'я

### Опис

```methodsynopsis
public ZipArchive::getCommentName(string $name, int $flags = 0): string|false
```

Повертає коментар елемента, використовуючи його ім'я.

### Список параметрів

`name`

Ім'я елемент.

`flags`

Якщо прапор встановлений у **`ZipArchive::FL_UNCHANGED`**, повертається оригінальний незмінений коментар

### Значення, що повертаються

Повертає коментар при успіху або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вивести коментар елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test1.zip');
if ($res === TRUE) {
    var_dump($zip->getCommentName('test/entry1.txt'));
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```