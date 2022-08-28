Перейменовує елемент на його ім'я

-   [« ZipArchive::renameIndex](ziparchive.renameindex.html)
    
-   [ZipArchive::replaceFile »](ziparchive.replacefile.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Перейменовує елемент на його ім'я
    

# ZipArchive::renameName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::renameName — Перейменовує елемент на ім'я

### Опис

```methodsynopsis
public ZipArchive::renameName(string $name, string $new_name): bool
```

Перейменовує елемент, заданий на ім'я.

### Список параметрів

`name`

Назва елемента для перейменування.

`new_name`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перейменування одного елемента**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    $zip->renameName('currentname.txt','newname.txt');
    $zip->close();
} else {
    echo 'ошибка с кодом:' . $res;
}
?>
```