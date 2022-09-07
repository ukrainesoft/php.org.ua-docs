---
navigation:
  - swoole-http-request.rawcontent.md: '« SwooleHttpRequest::rawcontent'
  - swoole-http-response.cookie.md: 'SwooleHttpResponse::cookie »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleHttpResponse
---
# Клас SwooleHttpResponse

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Http\Response
     
     {


    /* Методы */
    
   public cookie(    string $name,    string $value = ?,    string $expires = ?,    string $path = ?,    string $domain = ?,    string $secure = ?,    string $httponly = ?): string
public __destruct(): void
public end(string $content = ?): void
public gzip(string $compress_level = ?): ReturnType
public header(string $key, string $value, string $ucwords = ?): void
public initHeader(): ReturnType
public rawcookie(    string $name,    string $value = ?,    string $expires = ?,    string $path = ?,    string $domain = ?,    string $secure = ?,    string $httponly = ?): ReturnType
public sendfile(string $filename, int $offset = ?): ReturnType
public status(string $http_code): ReturnType
public write(string $content): void

   }
```

## Зміст

-   [SwooleHttpResponse::cookie](swoole-http-response.cookie.md) — Встановлює cookie HTTP-відповіді
-   [SwooleHttpResponse::destruct](swoole-http-response.destruct.md) — Знищує HTTP-відповідь
-   [SwooleHttpResponse::end](swoole-http-response.end.md) — Надсилає дані HTTP-запиту та завершує відповідь
-   [SwooleHttpResponse::gzip](swoole-http-response.gzip.md) — Включає gzip-стиснення відповіді.
-   [SwooleHttpResponse::header](swoole-http-response.header.md) — Встановлює заголовки HTTP-відповіді
-   [SwooleHttpResponse::initHeader](swoole-http-response.initheader.md) — Ініціювати заголовок HTTP-відповіді
-   [SwooleHttpResponse::rawcookie](swoole-http-response.rawcookie.md) — Встановлює необроблені cookie у HTTP-відповідь
-   [SwooleHttpResponse::sendfile](swoole-http-response.sendfile.md) — Надсилає файл через HTTP-відповідь
-   [SwooleHttpResponse::status](swoole-http-response.status.md) — Встановлює код стану HTTP-відповіді
-   [SwooleHttpResponse::write](swoole-http-response.write.md) — Додає вміст тіла HTTP у відповідь HTTP
