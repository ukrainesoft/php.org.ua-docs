---
navigation:
  - zlib.constants.md: « Зумовлені константи
  - ref.zlib.md: Функції Zlib »
  - index.md: PHP Manual
  - book.zlib.md: Zlib
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

У цьому прикладі відкривається тимчасовий файл, записується рядок, а потім двічі виводиться вміст.

**Приклад #1 Приклад використання Zlib**

```php
<?php

$filename = tempnam('/tmp', 'zlibtest') . '.gz';
echo "<html>\n<head></head>\n<body>\n<pre>\n";
$s = "Только тест, тест, тест, тест, тест, тест, тест, тест!\n";

// Открытие файла для записи с максимальным сжатием
$zp = gzopen($filename, "w9");

// Запись строки в файл
gzwrite($zp, $s);

// Закрытие файла
gzclose($zp);

// Открытие файла для чтения
$zp = gzopen($filename, "r");

// Чтение трёх символов
echo gzread($zp, 3);

// Вывод до конца файла, а затем закрытие файла
gzpassthru($zp);
gzclose($zp);

echo "\n";

// Открытие файла и вывод содержимого (во второй раз)
if (readgzfile($filename) != strlen($s)) {
     echo "Возникла ошибка с функциями zlib!";
}
unlink($filename);
echo "</pre>\n</body>\n</html>\n";

?>
```

**Приклад #2 Робота з API інкрементальної компресії та декомпресії**

```php
<?php

// Выполнение компрессии GZIP:
$deflateContext = deflate_init(ZLIB_ENCODING_GZIP);
$compressed = deflate_add($deflateContext, "Данные для сжатия", ZLIB_NO_FLUSH);
$compressed .= deflate_add($deflateContext, ", больше данных", ZLIB_NO_FLUSH);
$compressed .= deflate_add($deflateContext, "и ещё больше данных!", ZLIB_FINISH);

// Выполнение декомпрессии GZIP:
$inflateContext = inflate_init(ZLIB_ENCODING_GZIP);
$uncompressed = inflate_add($inflateContext, $compressed, ZLIB_NO_FLUSH);
$uncompressed .= inflate_add($inflateContext, NULL, ZLIB_FINISH);
echo $uncompressed;
?>
```

Результат виконання наведеного прикладу:

```
Данные для сжатия, больше данных и ещё больше данных!
```
