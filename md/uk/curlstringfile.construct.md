Створює об'єкт CURLStringFile

-   [« CURLStringFile](class.curlstringfile.html)
    
-   [Event »](book.event.html)
    
-   [PHP Manual](index.html)
    
-   [CURLStringFile](class.curlstringfile.html)
    
-   Створює об'єкт CURLStringFile
    

# CURLStringFile::construct

(PHP 8> = 8.1.0)

CURLStringFile::construct — Створює об'єкт CURLStringFile

### Опис

public **CURLStringFile::construct**(string `$data`, string `$postname`, string `$mime` = "application/octet-stream")

Створює об'єкт [CURLStringFile](class.curlstringfile.html), який використовується для завантаження файлу за допомогою **`CURLOPT_POSTFIELDS`**

### Список параметрів

`data`

Вміст для завантаження.

`postname`

Ім'я файлу, який буде використовуватися в завантажених даних.

`mime`

MIME-тип файлу (за замовчуванням `application/octet-stream`

### Приклади

**Приклад #1 Приклад використання **CURLStringFile::construct()****

```php
<?php
/* http://example.com/upload.php:
<?php
var_dump($_FILES);
var_dump(file_get_contents($_FILES['test_string']['tmp_name']));
?>
*/

// Создание дескриптора cURL
$ch = curl_init('http://example.com/upload.php');

// Создание объекта CURLStringFile
$cstringfile = new CURLStringFile('тестовое содержимое для загрузки','test.txt','text/plain');

// Назначение данных для POST-запроса
$data = array('test_string' => $cstringfile);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_POSTFIELDS, $data);

// Выполнение дескриптора
curl_exec($ch);
?>
```

Результат виконання цього прикладу:

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

-   [curlsetopt()](function.curl-setopt.html) - Встановлює параметр для сеансу CURL