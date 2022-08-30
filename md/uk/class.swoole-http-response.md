Клас SwooleHttpResponse

-   [« SwooleHttpRequest::rawcontent](swoole-http-request.rawcontent.html)
    
-   [SwooleHttpResponse::cookie »](swoole-http-response.cookie.html)
    
-   [PHP Manual](index.md)
    
-   [Swoole](book.swoole.md)
    
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

-   [SwooleHttpResponse::cookie](swoole-http-response.cookie.html) — Встановлює cookie HTTP-відповіді
-   [SwooleHttpResponse::destruct](swoole-http-response.destruct.html) — Знищує HTTP-відповідь
-   [SwooleHttpResponse::end](swoole-http-response.end.html) — Надсилає дані HTTP-запиту та завершує відповідь
-   [SwooleHttpResponse::gzip](swoole-http-response.gzip.html) — Включає gzip-стиснення відповіді.
-   [SwooleHttpResponse::header](swoole-http-response.header.html) — Встановлює заголовки HTTP-відповіді
-   [SwooleHttpResponse::initHeader](swoole-http-response.initheader.html) — Ініціювати заголовок HTTP-відповіді
-   [SwooleHttpResponse::rawcookie](swoole-http-response.rawcookie.html) — Встановлює необроблені cookie у HTTP-відповідь
-   [SwooleHttpResponse::sendfile](swoole-http-response.sendfile.html) — Надсилає файл через HTTP-відповідь
-   [SwooleHttpResponse::status](swoole-http-response.status.html) — Встановлює код стану HTTP-відповіді
-   [SwooleHttpResponse::write](swoole-http-response.write.html) — Додає вміст тіла HTTP у відповідь HTTP