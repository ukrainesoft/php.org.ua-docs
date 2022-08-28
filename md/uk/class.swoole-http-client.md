Клас SwooleHttpClient

-   [« Swoole\\Exception](class.swoole-exception.html)
    
-   [Swoole\\Http\\Client::addFile »](swoole-http-client.addfile.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleHttpClient
    

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

-   [Swoole\\Http\\Client::addFile](swoole-http-client.addfile.html) — Додає файл до форми повідомлення
-   [Swoole\\Http\\Client::close](swoole-http-client.close.html) - Закриває http-з'єднання
-   [Swoole\\Http\\Client::\_\_construct](swoole-http-client.construct.html) - Створює асинхронний HTTP-клієнт
-   [Swoole\\Http\\Client::\_\_destruct](swoole-http-client.destruct.html) — Знищує HTTP-клієнт
-   [Swoole\\Http\\Client::download](swoole-http-client.download.html) — Завантажує файл із віддаленого сервера
-   [Swoole\\Http\\Client::execute](swoole-http-client.execute.html) — Надсилає HTTP-запит після встановлення параметрів
-   [Swoole\\Http\\Client::get](swoole-http-client.get.html) — Надсилає HTTP-запит GET на віддалений сервер
-   [Swoole\\Http\\Client::isConnected](swoole-http-client.isconnected.html) — Перевіряє, чи підключено HTTP-з'єднання.
-   [Swoole\\Http\\Client::on](swoole-http-client.on.html) - Реєструє callback-функцію на ім'я події
-   [Swoole\\Http\\Client::post](swoole-http-client.post.html) — Надсилає HTTP-запит POST на віддалений сервер
-   [Swoole\\Http\\Client::push](swoole-http-client.push.html) — Передає дані клієнту websocket
-   [Swoole\\Http\\Client::set](swoole-http-client.set.html) — Оновлює параметри HTTP-клієнта
-   [Swoole\\Http\\Client::setCookies](swoole-http-client.setcookies.html) — Встановлює cookies для HTTP-запиту
-   [Swoole\\Http\\Client::setData](swoole-http-client.setdata.html) — Встановлює дані тіла HTTP-запиту
-   [Swoole\\Http\\Client::setHeaders](swoole-http-client.setheaders.html) — Встановлює заголовки HTTP-запиту
-   [Swoole\\Http\\Client::setMethod](swoole-http-client.setmethod.html) — Встановлює метод HTTP-запиту
-   [Swoole\\Http\\Client::upgrade](swoole-http-client.upgrade.html) — Оновлення до протоколу websocket