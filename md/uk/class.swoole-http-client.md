---
navigation:
  - class.swoole-exception.md: « SwooleException
  - swoole-http-client.addfile.md: 'SwooleHttpClient::addFile »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleHttpClient
---
# Клас SwooleHttpClient

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Http\Client
     
     {

    /* Свойства */
    
     public
      $errCode;

    public
      $sock;



    /* Методы */
    
   public addFile(    string $path,    string $name,    string $type = ?,    string $filename = ?,    string $offset = ?): void
public close(): void
public __destruct(): void
public download(    string $path,    string $file,    callable $callback,    int $offset = ?): void
public execute(string $path, string $callback): void
public get(string $path, callable $callback): void
public isConnected(): bool
public on(string $event_name, callable $callback): void
public post(string $path, string $data, callable $callback): void
public push(string $data, string $opcode = ?, string $finish = ?): void
public set(array $settings): void
public setCookies(array $cookies): void
public setData(string $data): ReturnType
public setHeaders(array $headers): void
public setMethod(string $method): void
public upgrade(string $path, string $callback): void

   }
```

## Властивості

errCode

sock

## Зміст

-   [SwooleHttpClient::addFile](swoole-http-client.addfile.md) — Додає файл до форми повідомлення
-   [SwooleHttpClient::close](swoole-http-client.close.md) - Закриває http-з'єднання
-   [SwooleHttpClient::construct](swoole-http-client.construct.md) - Створює асинхронний HTTP-клієнт
-   [SwooleHttpClient::destruct](swoole-http-client.destruct.md) — Знищує HTTP-клієнт
-   [SwooleHttpClient::download](swoole-http-client.download.md) — Завантажує файл із віддаленого сервера
-   [SwooleHttpClient::execute](swoole-http-client.execute.md) — Надсилає HTTP-запит після встановлення параметрів
-   [SwooleHttpClient::get](swoole-http-client.get.md) — Надсилає HTTP-запит GET на віддалений сервер
-   [SwooleHttpClient::isConnected](swoole-http-client.isconnected.md) — Перевіряє, чи підключено HTTP-з'єднання.
-   [SwooleHttpClient::on](swoole-http-client.on.md) - Реєструє callback-функцію на ім'я події
-   [SwooleHttpClient::post](swoole-http-client.post.md) — Надсилає HTTP-запит POST на віддалений сервер
-   [SwooleHttpClient::push](swoole-http-client.push.md) — Передає дані клієнту websocket
-   [SwooleHttpClient::set](swoole-http-client.set.md) — Оновлює параметри HTTP-клієнта
-   [SwooleHttpClient::setCookies](swoole-http-client.setcookies.md) — Встановлює cookies для HTTP-запиту
-   [SwooleHttpClient::setData](swoole-http-client.setdata.md) — Встановлює дані тіла HTTP-запиту
-   [SwooleHttpClient::setHeaders](swoole-http-client.setheaders.md) — Встановлює заголовки HTTP-запиту
-   [SwooleHttpClient::setMethod](swoole-http-client.setmethod.md) — Встановлює метод HTTP-запиту
-   [SwooleHttpClient::upgrade](swoole-http-client.upgrade.md) — Оновлення до протоколу websocket
