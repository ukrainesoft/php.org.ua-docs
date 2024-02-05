---
navigation:
  - zip.constants.md: « Зумовлені константи
  - class.ziparchive.md: ZipArchive »
  - index.md: PHP Manual
  - book.zip.md: Zip
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Створення Zip-архіву**

```php
<?php

$zip = new ZipArchive();
$filename = "./test112.zip";

if ($zip->open($filename, ZipArchive::CREATE)!==TRUE) {
    exit("Невозможно открыть <$filename>\n");
}

$zip->addFromString("testfilephp.txt" . time(), "#1 Это тестовая строка добавляется в качестве testfilephp.txt.\n");
$zip->addFromString("testfilephp2.txt" . time(), "#2 Это тестовая строка добавляется в качестве testfilephp2.txt.\n");
$zip->addFile($thisdir . "/too.php","/testfromfile.php");
echo "numfiles: " . $zip->numFiles . "\n";
echo "status:" . $zip->status . "\n";
$zip->close();
?>
```

**Приклад #2 Зібрати та відобразити докладну інформацію про архів**

```php
<?php
$za = new ZipArchive();

$za->open('test_with_comment.zip');
print_r($za);
var_dump($za);
echo "numFiles: " . $za->numFiles . "\n";
echo "status: " . $za->status  . "\n";
echo "statusSys: " . $za->statusSys . "\n";
echo "filename: " . $za->filename . "\n";
echo "comment: " . $za->comment . "\n";

for ($i=0; $i<$za->numFiles;$i++) {
    echo "index: $i\n";
    print_r($za->statIndex($i));
}
echo "numFile:" . $za->numFiles . "\n";
?>
```

**Приклад #3 Використання обгортки потоку Zip, читання метаінформації OpenOffice**

```php
<?php
$reader = new XMLReader();

$reader->open('zip://' . dirname(__FILE__) . '/test.odt#meta.xml');
$odt_meta = array();
while ($reader->read()) {
    if ($reader->nodeType == XMLREADER::ELEMENT) {
        $elm = $reader->name;
    } else {
        if ($reader->nodeType == XMLREADER::END_ELEMENT && $reader->name == 'office:meta') {
            break;
        }
        if (!trim($reader->value)) {
            continue;
        }
        $odt_meta[$elm] = $reader->value;
    }
}
print_r($odt_meta);
?>
```

Цей приклад використовує стару версію API (PHP 4), він відкриває ZIP-архів, читає кожен файл у архіві та виводить його вміст. Архів test2.zip, використаний у цьому прикладі, є одним із тестових архівів вихідного дистрибутива ZZIPlib.

**Приклад #4 Приклад використання Zip**

```php
<?php

$zip = zip_open("/tmp/test2.zip");

if ($zip) {
    while ($zip_entry = zip_read($zip)) {
        echo "Название:         " . zip_entry_name($zip_entry) . "\n";
        echo "Исходный размер:  " . zip_entry_filesize($zip_entry) . "\n";
        echo "Сжатый размер:    " . zip_entry_compressedsize($zip_entry) . "\n";
        echo "Метод сжатия:     " . zip_entry_compressionmethod($zip_entry) . "\n";

        if (zip_entry_open($zip, $zip_entry, "r")) {
            echo "Содержимое файла:\n";
            $buf = zip_entry_read($zip_entry, zip_entry_filesize($zip_entry));
            echo "$buf\n";

            zip_entry_close($zip_entry);
        }
        echo "\n";

    }

    zip_close($zip);

}
?>
```
