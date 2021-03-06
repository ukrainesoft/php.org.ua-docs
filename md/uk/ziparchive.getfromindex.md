- [« ZipArchive::getExternalAttributesName](ziparchive.getexternalattributesname.md)
- [ZipArchive::getFromName »](ziparchive.getfromname.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- Повертає вміст елемента за його індексом

# ZipArchive::getFromIndex

(PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.1.0)

ZipArchive::getFromIndex — Повертає вміст елемента за його індексом

### Опис

public **ZipArchive::getFromIndex**(int `$index`, int `$len` = 0, int
`$flags` = 0): string\|false

Повертає вміст елемента за його індексом.

### Список параметрів

`index`
Індекс елемент.

`len`
Розмір даних з елемента. Якщо `0`, вміст читається
повністю.

`flags`
Прапори, що використовуються для відкриття архіву. Можливо встановлено лише
одне нижченаведене значення.

- **`ZipArchive::FL_UNCHANGED`**

- **`ZipArchive::FL_COMPRESSED`**

### Значення, що повертаються

Повертає вміст елемента при успіху або **`false`** у разі
виникнення помилки.

### Приклади

**Приклад #1 Отримати вміст файлу**

` <?php$zip = new ZipArchive;if ($zip->open('test.zip') === TRUE) {    echo $zip->getFromIndex(2); $zip->close();} else {    echo 'помилка';}?> `

### Дивіться також

- [ZipArchive::getFromName()](ziparchive.getfromname.md) -
Повертає вміст елемента на його ім'я
