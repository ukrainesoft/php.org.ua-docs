Встановлює коментар до елемента, заданого на ім'я

-   [« ZipArchive::setCommentIndex](ziparchive.setcommentindex.md)
    
-   [ZipArchive::setCompressionIndex »](ziparchive.setcompressionindex.md)
    
-   [PHP Manual](index.md)
    
-   [ZipArchive](class.ziparchive.md)
    
-   Встановлює коментар до елемента, заданого на ім'я
    

# ZipArchive::setCommentName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::setCommentName — Встановлює коментар до елемента, заданого на ім'я

### Опис

```methodsynopsis
public ZipArchive::setCommentName(string $name, string $comment): bool
```

Встановлює коментар до елемента, заданого на ім'я.

### Список параметрів

`name`

Ім'я елемент.

`comment`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Відкриття архіву та встановлення коментарів до елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    $zip->setCommentName('entry1.txt', 'новая запись комментария');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```