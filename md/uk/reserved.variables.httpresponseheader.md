---
navigation:
  - reserved.variables.phperrormsg.md: « $php\_errormsg
  - reserved.variables.argc.md: $argc »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $http\_response\_header
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $http\_response\_header

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

$http\_response\_header — Заголовки відповідей HTTP

### Опис

Масив (array) $http\_response\_header похож на функцию[get\_headers()](function.get-headers.md)При использовании[обгортки HTTP](wrappers.http.md), $http\_response\_header буде заповнюватись заголовками відповіді HTTP. $http\_response\_header будет создан в[локальної області видимості](language.variables.scope.md)

### Приклади

**Приклад #1 Приклад $http\_response\_header**

```php
<?php
function get_contents() {
  file_get_contents("http://example.com");
  var_dump($http_response_header); // переменная заполняется в локальной области видимости
}
get_contents();
var_dump($http_response_header); // вызов функции get_contents() не заполняет переменную вне области видимости функции
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(9) {
  [0]=>
  string(15) "HTTP/1.1 200 OK"
  [1]=>
  string(35) "Date: Sat, 12 Apr 2008 17:30:38 GMT"
  [2]=>
  string(29) "Server: Apache/2.2.3 (CentOS)"
  [3]=>
  string(44) "Last-Modified: Tue, 15 Nov 2005 13:24:10 GMT"
  [4]=>
  string(27) "ETag: "280100-1b6-80bfd280""
  [5]=>
  string(20) "Accept-Ranges: bytes"
  [6]=>
  string(19) "Content-Length: 438"
  [7]=>
  string(17) "Connection: close"
  [8]=>
  string(38) "Content-Type: text/html; charset=UTF-8"
}

Warning: Undefined variable $http_response_header
NULL
```
