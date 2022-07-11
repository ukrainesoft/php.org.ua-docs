- [«Зумовлені константи](zlib.constants.md)
- [Функції Zlib»](ref.zlib.md)

- [PHP Manual](index.md)
- [Zlib](book.zlib.md)
- Приклади

# Приклади

У цьому прикладі відкривається тимчасовий файл, записується рядок, а
потім двічі виводиться вміст.

**Приклад #1 Приклад використання Zlib**

` <?php$filename = tempnam('/tmp', 'zlibtest') . '.gz';echo "<html>
<head></head>
<body>
<pre>
";$s = "Тільки тест, тест, тест, тест, тест, тест, тест, тест!
";// Відкриття файлу для запису з максимальним стисненням$zp = gzopen($filename, "w9");// Запис рядки в файлgzwrite($zp, $s);// | файлу для читання $ zp = = gzopen ($ filename, "")"; ;echo "
";// Відкриття файлу і виведення вмісту (у другий раз)if (readgzfile($filename) != strlen($s)) {     echo "Виникла помилка з| /pre>
</body>
</html>
";?> `

**Приклад #2 Робота з API інкрементальної компресії та декомпресії**

`<?php// Виконання компресії GZIP:$deflateContext = deflate_init(ZLIB_ENCODING_GZIP); ZLIB_NO_FLUSH);$compressed .= deflate_add($deflateContext, "и ещё больше данных!", ZLIB_FINISH);// Выполнение декомпрессии GZIP:$inflateContext = inflate_init(ZLIB_ENCODING_GZIP);$uncompressed = inflate_add($inflateContext, $compressed, ZLIB_NO_FLUSH) ;$uncompressed .= inflate_add($inflateContext, NULL, ZLIB_FINISH);echo $uncompressed;?> `

Результат виконання цього прикладу:

Дані для стиснення, більше даних та ще більше даних!
