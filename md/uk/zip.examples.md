- [«Зумовлені константи](zip.constants.md)
- [ZipArchive »](class.ziparchive.md)

- [PHP Manual](index.md)
- [Zip](book.zip.md)
- Приклади

# Приклади

**Приклад #1 Створення Zip-архіву**

` <?php$zip = new ZipArchive();$filename = "./test112.zip";if ($zip->open($filename, ZipArchive::CREATE)!==TRUE) {     exit("Неможливо| <$filename>
");}$zip->addFromString("testfilephp.txt" . time(), "#1 Це тестовий рядок додається в якості testfilephp.txt.
");$zip->addFromString("testfilephp2.txt" . time(), "#2 Це тестовий рядок додається в якости testfilephp2.txt.
");$zip->addFile($thisdir . "/too.php","/testfromfile.php");echo "numfiles: " . $zip->numFiles . "
";echo "status:" . $zip->status . "
";$zip->close();?> `

**Приклад #2 Зібрати та відобразити докладну інформацію про архів**

` <?php$za = new ZipArchive();$za->open('test_with_comment.zip');print_r($za);var_dump($za);echo "numFiles: " . $za->numFiles . "
";echo "status: " . $za->status  . "
";echo "statusSys: " . $za->statusSys . "
";echo "filename: " . $za->filename . "
";echo "comment: " . $za->comment . "
";for ($i=0; $i<$za->numFiles;$i++) {    echo "index: $i
";    print_r($za->statIndex($i));}echo "numFile:" . $za->numFiles . "
";?> `

**Приклад #3 Використання обгортки потоку Zip, читання метаінформації
OpenOffice**

` <?php$reader = new XMLReader();$reader->open('zip://' . dirname(__FILE__) . '/test.odt#meta.xml');$odt_meta = array();while ($reader->read()) {   if ($reader->nodeType == XMLREADER::ELEMENT) {         $elm = $reader->name; } else {        if ($reader->nodeType == XMLREADER::END_ELEMENT && $reader->name == 'office:meta') {         | }        if (!trim($reader->value)) {            continue; }        $odt_meta[$elm] = $reader->value; }}print_r($odt_meta);?> `

Цей приклад використовує стару версію API (PHP 4), він відкриває
ZIP-архів читає кожен файл в архіві і виводить його вміст. Архів
`test2.zip`, використаний у цьому прикладі, є одним із тестових
архівів вихідного дистрибутива ZZIPlib

**Приклад #4 Приклад використання Zip**

` <?php$zip = zip_open("/tmp/test2.zip");if ($zip) {    while ($zip_entry = zip_read($zip)) {        echo "              zip_entry_name($zip_entry) . "
";        echo "Вихідний розмір:  " . zip_entry_filesize($zip_entry) . "
";        echo "Стиснутий розмір:    " . zip_entry_compressedsize($zip_entry) . "
";        echo "Метод стиснення:      " . zip_entry_compressionmethod($zip_entry) . "
";        if (zip_entry_open($zip, $zip_entry, "r")) {            echo "Вміст файлу:
";             $buf = zip_entry_read($zip_entry, zip_entry_filesize($zip_entry));             echo "$f
";             zip_entry_close($zip_entry);        }        echo "
";    }    zip_close($zip);}?> `
