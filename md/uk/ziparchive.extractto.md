---
navigation:
  - ziparchive.deletename.md: '« ZipArchive::deleteName'
  - ziparchive.getarchivecomment.md: 'ZipArchive::getArchiveComment »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::extractTo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::extractTo

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::extractTo — Витягує вміст архіву

### Опис

```methodsynopsis
public ZipArchive::extractTo(string $pathto, array|string|null $files = null): bool
```

Вилучення всього архіву або його частини у вказане місце призначення.

**Увага**

Дозволи за промовчанням для вилучених файлів та каталогів дають максимально широкий доступ. Це можна обмежити, встановивши поточну маску дозволів umask функцією [umask()](function.umask.md)

З міркувань безпеки вихідні дозволи не відновлюються . [Приклади](ziparchive.getexternalattributesindex.md#ziparchive.getexternalattributesindex.examples.perms) того, як їх відновити, показано на сторінці з описом методу [ZipArchive::getExternalAttributesIndex()](ziparchive.getexternalattributesindex.md)

### Список параметрів

`pathto`

Директорія, в яку потрібно отримувати файли.

`files`

Елементи для вилучення. Може приймати як значення, і масив записів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Вийняти весь вміст**

```php
<?php
$zip = new ZipArchive;
if ($zip->open('test.zip') === TRUE) {
    $zip->extractTo('/my/destination/dir/');
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

**Приклад #2 Вийняти два елементи**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test_im.zip');
if ($res === TRUE) {
    $zip->extractTo('/my/destination/dir/', array('pear_item.gif', 'testfromfile.php'));
    $zip->close();
    echo 'готово';
} else {
    echo 'ошибка';
}
?>
```

### Примітки

> **Зауваження** :
> 
> Файлові системи Windows NTFS не підтримують деякі символи в іменах файлів, зокрема `<|>*?":`. Імена файлів із точкою в кінці також не підтримуються. На відміну від деяких інструментів вилучення, цей метод не підтримує заміну цих символів на підкреслення, а натомість виникає помилка при вийманні таких файлів.
