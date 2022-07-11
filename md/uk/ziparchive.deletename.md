- [« ZipArchive::deleteIndex](ziparchive.deleteindex.md)
- [ZipArchive::extractTo »](ziparchive.extractto.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- Видаляє елемент в архіві, використовуючи його ім'я

# ZipArchive::deleteName

(PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.5.0)

ZipArchive::deleteName — Видаляє елемент в архіві за допомогою його імені.

### Опис

public **ZipArchive::deleteName**(string `$name`): bool

Видаляє елемент (файл або каталог) в архіві за допомогою його імені.

### Список параметрів

`name`
Назва елемента для видалення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Видалити файл та каталог з архіву за допомогою імен**

` <?php$zip = new ZipArchive;if ($zip->open('test1.zip') === TRUE) {   $zip->deleteName('testfromfile.php'); $zip->deleteName('testDir/'); $zip->close(); echo 'готово';} else {    echo 'помилка';}?> `
