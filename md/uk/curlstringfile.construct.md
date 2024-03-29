---
navigation:
  - class.curlstringfile.md: « CURLStringFile
  - book.event.md: Event »
  - index.md: PHP Manual
  - class.curlstringfile.md: CURLStringFile
title: 'CURLStringFile::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CURLStringFile::\_\_construct

(PHP 8 >= 8.1.0)

CURLStringFile::\_\_construct — Створює об'єкт CURLStringFile

### Опис

public **CURLStringFile::\_\_construct**(string`$data`, string`$postname`, string`$mime` = "application/octet-stream")

Створює об'єкт [CURLStringFile](class.curlstringfile.md), який використовується для завантаження файлу за допомогою **`CURLOPT_POSTFIELDS`**

### Список параметрів

`data`

Вміст для завантаження.

`postname`

Ім'я файлу, який буде використовуватися в завантажених даних.

`mime`

MIME-тип файла (по умолчанию`application/octet-stream`

### Приклади

**Приклад #1 Приклад використання** CURLStringFile::\_\_construct()\*\*\*\*

```php
<?php
/* http://example.com/upload.php:
<?php
var_dump($_FILES);
var_dump(file_get_contents($_FILES['test_string']['tmp_name']));
?>
*/

// Создание дескриптора cURL
$ch = curl_init('http://example.com/upload.php');

// Создание объекта CURLStringFile
$cstringfile = new CURLStringFile('тестовое содержимое для загрузки','test.txt','text/plain');

// Назначение данных для POST-запроса
$data = array('test_string' => $cstringfile);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Выполнение дескриптора
curl_exec($ch);
?>
```

Результат виконання наведеного прикладу:

```
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
```

### Дивіться також

-   [curl\_setopt()](function.curl-setopt.md) \- Встановлює параметр для передачі cURL
