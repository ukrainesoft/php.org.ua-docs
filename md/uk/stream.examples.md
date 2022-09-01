---
navigation:
  - stream.errors.html: « Ошибки потока
  - stream.streamwrapper.example-1.html: 'Приклад класу, зареєстрованого як обгортка потоку »'
  - index.html: PHP Manual
  - book.stream.html: Потоки
title: Приклади
---
# Приклади

## Зміст

-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.md)

**Приклад #1 Використання [filegetcontents()](function.file-get-contents.md) для отримання даних із різних джерел**

```php
<?php
/* Чтение локального файла из /home/bar */
$localfile = file_get_contents("/home/bar/foo.txt");

/* То же самое с явным заданием схемы FILE */
$localfile = file_get_contents("file:///home/bar/foo.txt");

/* Чтение удалённого файла по адресу from www.example.com, используя HTTP */
$httpfile  = file_get_contents("http://www.example.com/foo.txt");

/* Чтение удалённого файла по адресу www.example.com, используя HTTPS */
$httpsfile = file_get_contents("https://www.example.com/foo.txt");

/* Чтение удалённого файла по адресу ftp.example.com, используя FTP */
$ftpfile   = file_get_contents("ftp://user:pass@ftp.example.com/foo.txt");

/* Чтение удалённого файла по адресу ftp.example.com, используя FTPS */
$ftpsfile  = file_get_contents("ftps://user:pass@ftp.example.com/foo.txt");
?>
```

**Приклад #2 Здійснення POST-запиту до https-сервера**

```php
<?php
/* Посылаем POST запрос на адрес https://secure.example.com/form_action.php
* Включаем элементы формы "foo" и "bar" с подходящими данными
*/

$sock = fsockopen("ssl://secure.example.com", 443, $errno, $errstr, 30);
if (!$sock) die("$errstr ($errno)\n");

$data = "foo=" . urlencode("Значение Foo") . "&bar=" . urlencode("Значение Bar");

fwrite($sock, "POST /form_action.php HTTP/1.0\r\n");
fwrite($sock, "Host: secure.example.com\r\n");
fwrite($sock, "Content-type: application/x-www-form-urlencoded\r\n");
fwrite($sock, "Content-length: " . strlen($data) . "\r\n");
fwrite($sock, "Accept: */*\r\n");
fwrite($sock, "\r\n");
fwrite($sock, $data);

$headers = "";
while ($str = trim(fgets($sock, 4096)))
$headers .= "$str\n";

echo "\n";

$body = "";
while (!feof($sock))
$body .= fgets($sock, 4096);

fclose($sock);
?>
```

**Приклад #3 Запис даних у стислий файл**

```php
<?php
/* Создаём сжатый файл с различными данными
* Файл можно прочитать с помощью потока compress.zlib или
* просто разархивировать из командной строки 'gzip -d foo-bar.txt.gz'
*/
$fp = fopen("compress.zlib://foo-bar.txt.gz", "wb");
if (!$fp) die("Невозможно создать файл.");

fwrite($fp, "Тестовые данные.\n");

fclose($fp);
?>
```
