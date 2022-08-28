Клас SwooleHttpResponse

-   [« Swoole\\Http\\Request::rawcontent](swoole-http-request.rawcontent.html)
    
-   [Swoole\\Http\\Response::cookie »](swoole-http-response.cookie.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleHttpResponse
    

# Клас SwooleHttpResponse

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Http\Response
     
     {


    /* Методы */
    
   public cookie(    string $name,    string $value = ?,    string $expires = ?,    string $path = ?,    string $domain = ?,    string $secure = ?,    string $httponly = ?): string
public __destruct(): void
public end(string $content = ?): void
public gzip(string $compress_level = ?): ReturnType
public header(string $key, string $value, string $ucwords = ?): void
public initHeader(): ReturnType
public rawcookie(    string $name,    string $value = ?,    string $expires = ?,    string $path = ?,    string $domain = ?,    string $secure = ?,    string $httponly = ?): ReturnType
public sendfile(string $filename, int $offset = ?): ReturnType
public status(string $http_code): ReturnType
public write(string $content): void

   }
```

## Зміст

-   [Swoole\\Http\\Response::cookie](swoole-http-response.cookie.html) — Встановлює cookie HTTP-відповіді
-   [Swoole\\Http\\Response::\_\_destruct](swoole-http-response.destruct.html) — Знищує HTTP-відповідь
-   [Swoole\\Http\\Response::end](swoole-http-response.end.html) — Надсилає дані HTTP-запиту та завершує відповідь
-   [Swoole\\Http\\Response::gzip](swoole-http-response.gzip.html) — Включає gzip-стиснення відповіді.
-   [Swoole\\Http\\Response::header](swoole-http-response.header.html) — Встановлює заголовки HTTP-відповіді
-   [Swoole\\Http\\Response::initHeader](swoole-http-response.initheader.html) — Ініціювати заголовок HTTP-відповіді
-   [Swoole\\Http\\Response::rawcookie](swoole-http-response.rawcookie.html) — Встановлює необроблені cookie у HTTP-відповідь
-   [Swoole\\Http\\Response::sendfile](swoole-http-response.sendfile.html) — Надсилає файл через HTTP-відповідь
-   [Swoole\\Http\\Response::status](swoole-http-response.status.html) — Встановлює код стану HTTP-відповіді
-   [Swoole\\Http\\Response::write](swoole-http-response.write.html) — Додає вміст тіла HTTP у відповідь HTTP