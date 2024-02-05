---
navigation:
  - class.swoole-exception.md: « Swoole\\Exception
  - swoole-http-client.addfile.md: 'Swoole\\Http\\Client::addFile »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Http\\Client
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Http\\Client

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

-   [Swoole\\Http\\Client::addFile](swoole-http-client.addfile.md)— Додає файл до форми повідомлення
-   [Swoole\\Http\\Client::close](swoole-http-client.close.md) \- Закриває http-з'єднання
-   [Swoole\\Http\\Client::\_\_construct](swoole-http-client.construct.md) \- Створює асинхронний HTTP-клієнт
-   [Swoole\\Http\\Client::\_\_destruct](swoole-http-client.destruct.md)— Знищує HTTP-клієнт
-   [Swoole\\Http\\Client::download](swoole-http-client.download.md)— Завантажує файл із віддаленого сервера
-   [Swoole\\Http\\Client::execute](swoole-http-client.execute.md)— Надсилає HTTP-запит після встановлення параметрів
-   [Swoole\\Http\\Client::get](swoole-http-client.get.md)— Надсилає HTTP-запит GET на віддалений сервер
-   [Swoole\\Http\\Client::isConnected](swoole-http-client.isconnected.md)— Перевіряє, чи підключено HTTP-з'єднання.
-   [Swoole\\Http\\Client::on](swoole-http-client.on.md) \- Реєструє callback-функцію на ім'я події
-   [Swoole\\Http\\Client::post](swoole-http-client.post.md)— Надсилає HTTP-запит POST на віддалений сервер
-   [Swoole\\Http\\Client::push](swoole-http-client.push.md)— Передає дані клієнту websocket
-   [Swoole\\Http\\Client::set](swoole-http-client.set.md)— Оновлює параметри HTTP-клієнта
-   [Swoole\\Http\\Client::setCookies](swoole-http-client.setcookies.md)— Встановлює cookies для HTTP-запиту
-   [Swoole\\Http\\Client::setData](swoole-http-client.setdata.md)— Встановлює дані тіла HTTP-запиту
-   [Swoole\\Http\\Client::setHeaders](swoole-http-client.setheaders.md)— Встановлює заголовки HTTP-запиту
-   [Swoole\\Http\\Client::setMethod](swoole-http-client.setmethod.md)— Встановлює метод HTTP-запиту
-   [Swoole\\Http\\Client::upgrade](swoole-http-client.upgrade.md)— Оновлення до протоколу websocket
