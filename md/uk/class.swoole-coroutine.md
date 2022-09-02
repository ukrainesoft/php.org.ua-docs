---
navigation:
  - swoole-connection-iterator.valid.md: '« SwooleConnectionIterator::valid'
  - swoole-coroutine.call-user-func-array.md: 'SwooleCoroutine::calluserfuncarray »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleCoroutine
---
# Клас SwooleCoroutine

(PECL swoole >= 2.0.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Coroutine
     
     {


    /* Методы */
    
   public static call_user_func_array(callable $callback, array $param_array): mixed
public static call_user_func(callable $callback, mixed ...$args): mixed
public static cli_wait(): ReturnType
public static create(): ReturnType
public Swoole\Coroutine\Client::close(): ReturnType
public Swoole\Coroutine\Client::connect(): ReturnType
public Swoole\Coroutine\Client::__destruct(): ReturnType
public Swoole\Coroutine\Client::getpeername(): ReturnType
public Swoole\Coroutine\Client::getsockname(): ReturnType
public Swoole\Coroutine\Client::isConnected(): ReturnType
public Swoole\Coroutine\Client::recv(): ReturnType
public Swoole\Coroutine\Client::send(): ReturnType
public Swoole\Coroutine\Client::sendfile(): ReturnType
public Swoole\Coroutine\Client::sendto(): ReturnType
public Swoole\Coroutine\Client::set(): ReturnType
public Swoole\Coroutine\Http\Client::addFile(): ReturnType
public Swoole\Coroutine\Http\Client::close(): ReturnType
public Swoole\Coroutine\Http\Client::__destruct(): ReturnType
public Swoole\Coroutine\Http\Client::execute(): ReturnType
public Swoole\Coroutine\Http\Client::get(): ReturnType
public Swoole\Coroutine\Http\Client::getDefer(): ReturnType
public Swoole\Coroutine\Http\Client::isConnected(): ReturnType
public Swoole\Coroutine\Http\Client::post(): ReturnType
public Swoole\Coroutine\Http\Client::recv(): ReturnType
public Swoole\Coroutine\Http\Client::set(): ReturnType
public Swoole\Coroutine\Http\Client::setCookies(): ReturnType
public Swoole\Coroutine\Http\Client::setData(): ReturnType
public Swoole\Coroutine\Http\Client::setDefer(): ReturnType
public Swoole\Coroutine\Http\Client::setHeaders(): ReturnType
public Swoole\Coroutine\Http\Client::setMethod(): ReturnType
public Swoole\Coroutine\MySQL::close(): ReturnType
public Swoole\Coroutine\MySQL::connect(): ReturnType
public Swoole\Coroutine\MySQL::__destruct(): ReturnType
public Swoole\Coroutine\MySQL::getDefer(): ReturnType
public Swoole\Coroutine\MySQL::query(): ReturnType
public Swoole\Coroutine\MySQL::recv(): ReturnType
public Swoole\Coroutine\MySQL::setDefer(): ReturnType
public static getuid(): ReturnType
public static resume(): ReturnType
public static suspend(): ReturnType

   }
```

## Зміст

-   [SwooleCoroutine::calluserfuncarray](swoole-coroutine.call-user-func-array.md) - Викликає callback-функцію з масивом параметрів
-   [SwooleCoroutine::calluserfunc](swoole-coroutine.call-user-func.md) - Викликає callback-функцію, задану першим параметром
-   [SwooleCoroutine::cliwait](swoole-coroutine.cli-wait.md) - Опис
-   [SwooleCoroutine::create](swoole-coroutine.create.md) - Опис
-   [SwooleCoroutineClient::close](swoole-coroutine-client.close.md) - Опис
-   [SwooleCoroutineClient::connect](swoole-coroutine-client.connect.md) - Опис
-   [SwooleCoroutineClient::construct](swoole-coroutine-client.construct.md) - Опис
-   [SwooleCoroutineClient::destruct](swoole-coroutine-client.destruct.md) - Опис
-   [SwooleCoroutineClient::getpeername](swoole-coroutine-client.getpeername.md) - Опис
-   [SwooleCoroutineClient::getsockname](swoole-coroutine-client.getsockname.md) - Опис
-   [SwooleCoroutineClient::isConnected](swoole-coroutine-client.isconnected.md) - Опис
-   [SwooleCoroutineClient::recv](swoole-coroutine-client.recv.md) - Опис
-   [SwooleCoroutineClient::send](swoole-coroutine-client.send.md) - Опис
-   [SwooleCoroutineClient::sendfile](swoole-coroutine-client.sendfile.md) - Опис
-   [SwooleCoroutineClient::sendto](swoole-coroutine-client.sendto.md) - Опис
-   [SwooleCoroutineClient::set](swoole-coroutine-client.set.md) - Опис
-   [SwooleCoroutineHttpClient::addFile](swoole-coroutine-http-client.addfile.md) - Опис
-   [SwooleCoroutineHttpClient::close](swoole-coroutine-http-client.close.md) - Опис
-   [SwooleCoroutineHttpClient::construct](swoole-coroutine-http-client.construct.md) - Опис
-   [SwooleCoroutineHttpClient::destruct](swoole-coroutine-http-client.destruct.md) - Опис
-   [SwooleCoroutineHttpClient::execute](swoole-coroutine-http-client.execute.md) - Опис
-   [SwooleCoroutineHttpClient::get](swoole-coroutine-http-client.get.md) - Опис
-   [SwooleCoroutineHttpClient::getDefer](swoole-coroutine-http-client.getdefer.md) - Опис
-   [SwooleCoroutineHttpClient::isConnected](swoole-coroutine-http-client.isconnected.md) - Опис
-   [SwooleCoroutineHttpClient::post](swoole-coroutine-http-client.post.md) - Опис
-   [SwooleCoroutineHttpClient::recv](swoole-coroutine-http-client.recv.md) - Опис
-   [SwooleCoroutineHttpClient::set](swoole-coroutine-http-client.set.md) - Опис
-   [SwooleCoroutineHttpClient::setCookies](swoole-coroutine-http-client.setcookies.md) - Опис
-   [SwooleCoroutineHttpClient::setData](swoole-coroutine-http-client.setdata.md) - Опис
-   [SwooleCoroutineHttpClient::setDefer](swoole-coroutine-http-client.setdefer.md) - Опис
-   [SwooleCoroutineHttpClient::setHeaders](swoole-coroutine-http-client.setheaders.md) - Опис
-   [SwooleCoroutineHttpClient::setMethod](swoole-coroutine-http-client.setmethod.md) - Опис
-   [SwooleCoroutineMySQL::close](swoole-coroutine-mysql.close.md) - Опис
-   [SwooleCoroutineMySQL::connect](swoole-coroutine-mysql.connect.md) - Опис
-   [SwooleCoroutineMySQL::construct](swoole-coroutine-mysql.construct.md) - Опис
-   [SwooleCoroutineMySQL::destruct](swoole-coroutine-mysql.destruct.md) - Опис
-   [SwooleCoroutineMySQL::getDefer](swoole-coroutine-mysql.getdefer.md) - Опис
-   [SwooleCoroutineMySQL::query](swoole-coroutine-mysql.query.md) - Опис
-   [SwooleCoroutineMySQL::recv](swoole-coroutine-mysql.recv.md) - Опис
-   [SwooleCoroutineMySQL::setDefer](swoole-coroutine-mysql.setdefer.md) - Опис
-   [SwooleCoroutine::getuid](swoole-coroutine.getuid.md) - Опис
-   [SwooleCoroutine::resume](swoole-coroutine.resume.md) - Опис
-   [SwooleCoroutine::suspend](swoole-coroutine.suspend.md) - Опис
