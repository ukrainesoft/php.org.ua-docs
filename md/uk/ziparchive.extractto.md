Витягує вміст архіву

-   [« ZipArchive::deleteName](ziparchive.deletename.html)
    
-   [ZipArchive::getArchiveComment »](ziparchive.getarchivecomment.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Витягує вміст архіву
    

# ZipArchive::extractTo

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::extractTo — Витягує вміст архіву

### Опис

```methodsynopsis
public ZipArchive::extractTo(string $pathto, array|string|null $files = null): bool
```

Вилучення всього архіву або його частини у вказане місце призначення.

**Увага**

Дозволи за промовчанням для вилучених файлів та каталогів надають максимально широкий доступ. Це можна обмежити встановленням поточного umask, який змінюється за допомогою [umask()](function.umask.html)

### Список параметрів

`pathto`

Місце призначення, куди виймати файли.

`files`

Елементи для вилучення. Може приймати як значення, і масив записів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вийняти весь вміст**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->extractTo('/my/destination/dir/');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

**Приклад #2 Вийняти два елементи**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test_im.zip');
if ($res === TRUE) {
    $zip->extractTo('/my/destination/dir/', array('pear_item.gif', 'testfromfile.php'));
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

### Примітки

> **Зауваження**
> 
> Файлові системи Windows NTFS не підтримують деякі символи в іменах файлів, зокрема `<|>*?":`. Імена файлів із точкою в кінці також не підтримуються. На відміну від деяких інструментів вилучення, цей метод не підтримує заміну цих символів на підкреслення, а натомість виникає помилка при вийманні таких файлів.