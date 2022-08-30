Встановлює коментар до ZIP-архіву

-   [« ZipArchive::replaceFile](ziparchive.replacefile.md)
    
-   [ZipArchive::setCommentIndex »](ziparchive.setcommentindex.md)
    
-   [PHP Manual](index.md)
    
-   [ZipArchive](class.ziparchive.md)
    
-   Встановлює коментар до ZIP-архіву
    

# ZipArchive::setArchiveComment

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.4.0)

ZipArchive::setArchiveComment — Встановлює коментар до ZIP-архіву

### Опис

```methodsynopsis
public ZipArchive::setArchiveComment(string $comment): bool
```

Встановлює коментар до ZIP-архіву.

### Список параметрів

`comment`

Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення архіву та встановлення коментарів**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip', ZipArchive::CREATE);
if ($res === TRUE) {
    $zip->addFromString('test.txt', 'содержимое файла');
    $zip->setArchiveComment('новый комментарий архива');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```