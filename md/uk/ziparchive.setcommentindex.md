- [« ZipArchive::setArchiveComment](ziparchive.setarchivecomment.md)
- [ZipArchive::setCommentName »](ziparchive.setcommentname.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- Встановлює коментар до елемента за його індексом

# ZipArchive::setCommentIndex

(PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.4.0)

ZipArchive::setCommentIndex — Встановлює коментар до елементу з
його індексу

### Опис

public **ZipArchive::setCommentIndex**(int `$index`, string `$comment`):
bool

Встановлює коментар до елемента за його індексом.

### Список параметрів

`index`
Індекс елемент.

`comment`
Зміст коментаря.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Відкриває архів та встановлює коментар до елемента**

` <?php$zip = new ZipArchive;$res = $zip->open('test.zip');if ($res === TRUE) {    $zip->setCommentIndex(2, 'новий запис коментар' ; $zip->close(); echo 'готово';} else {    echo 'помилка';}?> `
