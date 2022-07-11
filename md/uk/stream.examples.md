- [« Помилки потоку](stream.errors.md)
- [Приклад класу, зареєстрованого як обгортка потоку »](stream.streamwrapper.example-1.md)

- [PHP Manual](index.md)
- [Потоки](book.stream.md)
- Приклади

# Приклади

## Зміст

- [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.md)

**Приклад #1 Використання
[file_get_contents()](function.file-get-contents.md) для отримання
даних із різних джерел**

` <?php/* Читання локального файла із /home/bar */$localfile = file_get_contents("/home/bar/foo.txt"); "file:///home/bar/foo.txt");/* Читання віддаленого файлу за адресою from www.example.com, використовуючи HTTP */$httpfile  = file_get_contents("http://www.example.com/ foo.txt");/* Читання віддаленого файлу за адресою www.example.com, використовуючи HTTPS */$httpsfile = file_get_contents("https://www.example.com/foo.txt");  за адресою ftp.example.com, використовуючи FTP */$ftpfile   = file_get_contents("ftp://user:pass@ftp.example.com/foo.txt");/* Читання віддаленого файлу по . , використовуючи FTPS */$ftpsfile  = file_get_contents("ftps://user:pass@ftp.example.com/foo.txt");?> `

**Приклад #2 Здійснення POST-запиту до https-сервера**

` <?php/* Посилаємо POST запит на адресу https://secure.example.com/form_action.php* Включаємо елементи форми "foo" і "bar" з підходящими даними*/$sock en secure.example.com", 443, $errno, $errstr, 30);if (!$sock) die("$errstr ($errno)
");$data = "foo=" . urlencode("Значення Foo") . "&bar=" . urlencode("Значення Bar");fwrite($sock, "POST /form_action.php HTTP/1.
");fwrite($sock, "Host: secure.example.com
");fwrite($sock, "Content-type: application/x-www-form-urlencoded
");fwrite($sock, "Content-length: " . strlen($data) . "
");fwrite($sock, "Accept: */*
");fwrite($sock, "
");fwrite($sock, $data);$headers = "";while ($str = trim(fgets($sock, 4096)))$headers .= "$str
";echo "
";$body = "";while (!feof($sock))$body .= fgets($sock, 4096);fclose($sock);?> `

**Приклад #3 Запис даних у стислий файл**

` <?php/* Створюємо стиснутий файл з різними даними* Файл можна прочитати з допомогою потоку compress.zlib або* просто fox fox| .zlib://foo-bar.txt.gz", "wb");if (!$fp) die("Неможливо створити файл.");fwrite($fp, "Тестові дані.
");fclose($fp);?> `
