---
navigation:
  - swoole-http-request.rawcontent.md: '« Swoole\\Http\\Request::rawcontent'
  - swoole-http-response.cookie.md: 'Swoole\\Http\\Response::cookie »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Http\\Response
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Http\\Response

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

-   [Swoole\\Http\\Response::cookie](swoole-http-response.cookie.md)— Встановлює cookie HTTP-відповіді
-   [Swoole\\Http\\Response::\_\_destruct](swoole-http-response.destruct.md)— Знищує HTTP-відповідь
-   [Swoole\\Http\\Response::end](swoole-http-response.end.md)— Надсилає дані HTTP-запиту та завершує відповідь
-   [Swoole\\Http\\Response::gzip](swoole-http-response.gzip.md)— Включає gzip-стиснення відповіді.
-   [Swoole\\Http\\Response::header](swoole-http-response.header.md)— Встановлює заголовки HTTP-відповіді
-   [Swoole\\Http\\Response::initHeader](swoole-http-response.initheader.md)— Ініціювати заголовок HTTP-відповіді
-   [Swoole\\Http\\Response::rawcookie](swoole-http-response.rawcookie.md)— Встановлює необроблені cookie у HTTP-відповідь
-   [Swoole\\Http\\Response::sendfile](swoole-http-response.sendfile.md)— Надсилає файл через HTTP-відповідь
-   [Swoole\\Http\\Response::status](swoole-http-response.status.md)— Встановлює код стану HTTP-відповіді
-   [Swoole\\Http\\Response::write](swoole-http-response.write.md)— Додає вміст тіла HTTP у відповідь HTTP
