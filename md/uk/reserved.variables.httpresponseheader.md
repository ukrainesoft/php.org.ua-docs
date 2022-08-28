Заголовки відповідей HTTP

-   [« $php\_errormsg](reserved.variables.phperrormsg.html)
    
-   [$argc »](reserved.variables.argc.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые переменные](reserved.variables.html)
    
-   Заголовки відповідей HTTP
    

# $httpresponseheader

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

$httpresponseheader — Заголовки відповідей HTTP

### Опис

Масив (array) $httpresponseheader схожий на функцію [get\_headers()](function.get-headers.html). При використанні [обёртки HTTP](wrappers.http.html), $httpresponseheader буде заповнюватись заголовками відповіді HTTP. $httpresponseheader буде створено в [локальной области видимости](language.variables.scope.html)

### Приклади

**Приклад #1 Приклад $httpresponseheader**

```php
<?php
function get_contents() {
  file_get_contents("http://example.com");
  var_dump($http_response_header);
}
get_contents();
var_dump($http_response_header);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
NULL
```