- [«CURLStringFile](class.curlstringfile.md)
- [Event »](book.event.md)

- [PHP Manual](index.md)
- [CURLStringFile](class.curlstringfile.md)
- Створює об'єкт CURLStringFile

# CURLStringFile::\_\_construct

(PHP 8 \>= 8.1.0)

CURLStringFile::\_\_construct — Створює об'єкт CURLStringFile

### Опис

public **CURLStringFile::\_\_construct**(string `$data`, string
`$postname`, string `$mime` = "application/octet-stream")

Створює об'єкт [CURLStringFile](class.curlstringfile.md), який
використовується для завантаження файлу за допомогою **CURLOPT_POSTFIELDS**.

### Список параметрів

`data`
Вміст для завантаження.

`postname`
Ім'я файлу, який буде використовуватися в даних, що завантажуються.

`mime`
MIME-тип файлу (за замовчуванням `application/octet-stream`).

### Приклади

**Приклад #1 Приклад використання **CURLStringFile::\_\_construct()****

` <?php/* http://example.com/upload.php:<?phpvar_dump($_FILES);var_dump(file_get_contents($_FILES['test_string']['tmp_name']));?>*// / Створення дескриптора cURL$ch = curl_init('http://example.com/upload.php');// Створення об'єкта CURLStringFile$cstringfile = new CURLStringFile('тестовий вміст' t''t''t'' /plain');//Призначення даних для POST-запиту$data = array('test_string' => $cstringfile);curl_setopt($ch, CURLOPT_POST, 1);curl_setopt($ch, CURLOPT_$ Виконання дескриптораcurl_exec($ch);?> `

Результат виконання цього прикладу:

array(1) {
["test_string"]=>
array(5) {
["name"]=>
string(8) "test.txt"
["type"]=>
string(10) "text/plain"
["tmp_name"]=>
string(14) "/tmp/phpTtaoCz"
["error"]=>
int(0)
["size"]=>
int(20)
}
}
string(20) "test upload contents"

### Дивіться також

- [curl_setopt()](function.curl-setopt.md) - Встановлює параметр
для сеансу CURL
