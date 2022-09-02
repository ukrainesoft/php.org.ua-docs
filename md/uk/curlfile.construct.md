---
navigation:
  - class.curlfile.md: « CURLFile
  - curlfile.getfilename.md: 'CURLFile::getFilename »'
  - index.md: PHP Manual
  - class.curlfile.md: CURLFile
title: 'CURLFile::construct'
---
# CURLFile::construct

# curlfilecreate

(PHP 5> = 5.5.0, PHP 7, PHP 8)

CURLFile::construct - curlfilecreate — Створює об'єкт CURLFile

### Опис

Об'єктно-орієнтований стиль

public **CURLFile::construct**(string `$filename`, ?string `$mime_type` **`null`**, ?string `$posted_filename` **`null`**

Процедурний стиль

```methodsynopsis
curl_file_create(string $filename, ?string $mime_type = null, ?string $posted_filename = null): CURLFile
```

Створює об'єкт [CURLFile](class.curlfile.md), що використовується для завантаження файлу з використанням опції **`CURLOPT_POSTFIELDS`**

### Список параметрів

`filename`

Шлях до файлу, який буде завантажено

`mime_type`

Mime-тип файлу.

`posted_filename`

Ім'я файлу при надсиланні методом POST.

### Значення, що повертаються

Повертає об'єкт типу [CURLFile](class.curlfile.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `mime_type` і `posted_filename` тепер припускають значення null; раніше значенням за умовчанням був `0` |

### Приклади

**Приклад #1 Приклад використання **CURLFile::construct()****

Об'єктно-орієнтований стиль

```php
<?php
/* http://example.com/upload.php:
<?php var_dump($_FILES); ?>
*/

// Создаём дескриптор cURL
$ch = curl_init('http://example.com/upload.php');

// Создаём объект CURLFile
$cfile = new CURLFile('cats.jpg','image/jpeg','test_name');

// Устанавливаем данные для POST
$data = array('test_file' => $cfile);
curl_setopt($ch, CURLOPT_POST,1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Запускаем дескриптор на выполнение
curl_exec($ch);
?>
```

Процедурний стиль

```php
<?php
/* http://example.com/upload.php:
<?php var_dump($_FILES); ?>
*/

// Создаём дескриптор cURL
$ch = curl_init('http://example.com/upload.php');

// Создаём объект CURLFile
$cfile = curl_file_create('cats.jpg','image/jpeg','test_name');

// Устанавливаем данные для POST
$data = array('test_file' => $cfile);
curl_setopt($ch, CURLOPT_POST,1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Запускаем дескриптор на выполнение
curl_exec($ch);
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["test_file"]=>
  array(5) {
    ["name"]=>
    string(9) "test_name"
    ["type"]=>
    string(10) "image/jpeg"
    ["tmp_name"]=>
    string(14) "/tmp/phpPC9Kbx"
    ["error"]=>
    int(0)
    ["size"]=>
    int(46334)
  }
}
```

**Приклад #2 Приклад використання **CURLFile::construct()** для завантаження кількох файлів**

Об'єктно-орієнтований стиль

```php
<?php
$request = curl_init('http://www.example.com/upload.php');
curl_setopt($request, CURLOPT_POST, true);
curl_setopt($request, CURLOPT_SAFE_UPLOAD, true);
curl_setopt($request, CURLOPT_POSTFIELDS, [
    'blob[0]' => new CURLFile(realpath('first-file.jpg'), 'image/jpeg'),
    'blob[1]' => new CURLFile(realpath('second-file.txt'), 'text/plain'),
    'blob[2]' => new CURLFile(realpath('third-file.exe'), 'application/octet-stream'),
]);
curl_setopt($request, CURLOPT_RETURNTRANSFER, true);

echo curl_exec($request);

var_dump(curl_getinfo($request));

curl_close($request);
```

Процедурний стиль

```php
<?php
// procedural
$request = curl_init('http://www.example.com/upload.php');
curl_setopt($request, CURLOPT_POST, true);
curl_setopt($request, CURLOPT_SAFE_UPLOAD, true);
curl_setopt($request, CURLOPT_POSTFIELDS, [
    'blob[0]' => curl_file_create(realpath('first-file.jpg'), 'image/jpeg'),
    'blob[1]' => curl_file_create(realpath('second-file.txt'), 'text/plain'),
    'blob[2]' => curl_file_create(realpath('third-file.exe'), 'application/octet-stream'),
]);
curl_setopt($request, CURLOPT_RETURNTRANSFER, true);

echo curl_exec($request);

var_dump(curl_getinfo($request));

curl_close($request);
```

Результат виконання цього прикладу:

```
array(26) {
  ["url"]=>
  string(31) "http://www.example.com/upload.php"
  ["content_type"]=>
  string(24) "text/html; charset=UTF-8"
  ["http_code"]=>
  int(200)
  ["header_size"]=>
  int(198)
  ["request_size"]=>
  int(196)
  ["filetime"]=>
  int(-1)
  ["ssl_verify_result"]=>
  int(0)
  ["redirect_count"]=>
  int(0)
  ["total_time"]=>
  float(0.060062)
  ["namelookup_time"]=>
  float(0.028575)
  ["connect_time"]=>
  float(0.029011)
  ["pretransfer_time"]=>
  float(0.029121)
  ["size_upload"]=>
  float(3230730)
  ["size_download"]=>
  float(811)
  ["speed_download"]=>
  float(13516)
  ["speed_upload"]=>
  float(53845500)
  ["download_content_length"]=>
  float(811)
  ["upload_content_length"]=>
  float(3230730)
  ["starttransfer_time"]=>
  float(0.030355)
  ["redirect_time"]=>
  float(0)
  ["redirect_url"]=>
  string(0) ""
  ["primary_ip"]=>
  string(13) "0.0.0.0"
  ["certinfo"]=>
  array(0) {
  }
  ["primary_port"]=>
  int(80)
  ["local_ip"]=>
  string(12) "0.0.0.0"
  ["local_port"]=>
  int(34856)
}
```

### Дивіться також

-   [curlsetopt()](function.curl-setopt.md) - Встановлює параметр для сеансу CURL
