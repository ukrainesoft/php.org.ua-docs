- [« ZipArchive::addGlob](ziparchive.addglob.md)
- [ZipArchive::clearError »](ziparchive.clearerror.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- Додати файли з директорії відповідно до шаблону регулярного
висловлювання PCRE

# ZipArchive::addPattern

(PHP 5 \>= 5.3.0, PHP 7, PHP 8, PECL zip \>= 1.9.0)

ZipArchive::addPattern — Додати файли з директорії відповідно до
шаблоном регулярного вираження PCRE

### Опис

public **ZipArchive::addPattern**(string `$pattern`, string `$path` =
".", array `$options` = []): array\|false

Додає файли з директорії відповідно до шаблону регулярного
висловлювання `pattern`. Операція не є рекурсивною. Шаблон застосовується тільки до
імен файлів.

### Список параметрів

`pattern` Шаблон [PCRE](book.pcre.md).

`path`
Директорія для сканування. За промовчанням вибирається поточна директорія.

`options`
Асоціативний масив параметрів, що приймаються
[ZipArchive::addGlob()](ziparchive.addglob.md).

### Значення, що повертаються

Масив (array) доданих файлів у разі успішного виконання або
**`false`** у разі виникнення помилки

### Приклади

**Приклад #1 Приклад використання **ZipArchive::addPattern()****

Додати до архіву всі текстові файли та файли скриптів PHP з поточної
директорії

` <?php$zip = new ZipArchive();$ret = $zip->open('application.zip', ZipArchive::CREATE || ZipArchive::OVERWRITE);if ($ret !== TRUE) { 'Помилка з кодом %d', $ret);} else {    $directory =realpath('.'); $options = array('add_path' => 'sources/', 'remove_path' => $directory); $zip->addPattern('/\.(?:php|txt)$/', $directory, $options); $zip->close();}?> `

### Дивіться також

- [ZipArchive::addFile()](ziparchive.addfile.md) - Додає до
ZIP-архів файл за вказаним шляхом
- [ZipArchive::addGlob()](ziparchive.addglob.md) - Додати файли з
директорії відповідно до шаблону
