---
navigation:
  - swoole-connection-iterator.valid.md: '« Swoole\\Connection\\Iterator::valid'
  - swoole-coroutine.call-user-func-array.md: 'Swoole\\Coroutine::call\_user\_func\_array »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Coroutine
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Coroutine

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

-   [Swoole\\Coroutine::call\_user\_func\_array](swoole-coroutine.call-user-func-array.md) \- Викликає callback-функцію з масивом параметрів
-   [Swoole\\Coroutine::call\_user\_func](swoole-coroutine.call-user-func.md) \- Викликає callback-функцію, задану першим параметром
-   [Swoole\\Coroutine::cli\_wait](swoole-coroutine.cli-wait.md) \- Опис
-   [Swoole\\Coroutine::create](swoole-coroutine.create.md) \- Опис
-   [Swoole\\Coroutine\\Client::close](swoole-coroutine-client.close.md) \- Опис
-   [Swoole\\Coroutine\\Client::connect](swoole-coroutine-client.connect.md) \- Опис
-   [Swoole\\Coroutine\\Client::\_\_construct](swoole-coroutine-client.construct.md) \- Опис
-   [Swoole\\Coroutine\\Client::\_\_destruct](swoole-coroutine-client.destruct.md) \- Опис
-   [Swoole\\Coroutine\\Client::getpeername](swoole-coroutine-client.getpeername.md) \- Опис
-   [Swoole\\Coroutine\\Client::getsockname](swoole-coroutine-client.getsockname.md) \- Опис
-   [Swoole\\Coroutine\\Client::isConnected](swoole-coroutine-client.isconnected.md) \- Опис
-   [Swoole\\Coroutine\\Client::recv](swoole-coroutine-client.recv.md) \- Опис
-   [Swoole\\Coroutine\\Client::send](swoole-coroutine-client.send.md) \- Опис
-   [Swoole\\Coroutine\\Client::sendfile](swoole-coroutine-client.sendfile.md) \- Опис
-   [Swoole\\Coroutine\\Client::sendto](swoole-coroutine-client.sendto.md) \- Опис
-   [Swoole\\Coroutine\\Client::set](swoole-coroutine-client.set.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::addFile](swoole-coroutine-http-client.addfile.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::close](swoole-coroutine-http-client.close.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::\_\_construct](swoole-coroutine-http-client.construct.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::\_\_destruct](swoole-coroutine-http-client.destruct.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::execute](swoole-coroutine-http-client.execute.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::get](swoole-coroutine-http-client.get.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::getDefer](swoole-coroutine-http-client.getdefer.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::isConnected](swoole-coroutine-http-client.isconnected.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::post](swoole-coroutine-http-client.post.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::recv](swoole-coroutine-http-client.recv.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::set](swoole-coroutine-http-client.set.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::setCookies](swoole-coroutine-http-client.setcookies.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::setData](swoole-coroutine-http-client.setdata.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::setDefer](swoole-coroutine-http-client.setdefer.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::setHeaders](swoole-coroutine-http-client.setheaders.md) \- Опис
-   [Swoole\\Coroutine\\Http\\Client::setMethod](swoole-coroutine-http-client.setmethod.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::close](swoole-coroutine-mysql.close.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::connect](swoole-coroutine-mysql.connect.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::\_\_construct](swoole-coroutine-mysql.construct.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::\_\_destruct](swoole-coroutine-mysql.destruct.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::getDefer](swoole-coroutine-mysql.getdefer.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::query](swoole-coroutine-mysql.query.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::recv](swoole-coroutine-mysql.recv.md) \- Опис
-   [Swoole\\Coroutine\\MySQL::setDefer](swoole-coroutine-mysql.setdefer.md) \- Опис
-   [Swoole\\Coroutine::getuid](swoole-coroutine.getuid.md) \- Опис
-   [Swoole\\Coroutine::resume](swoole-coroutine.resume.md) \- Опис
-   [Swoole\\Coroutine::suspend](swoole-coroutine.suspend.md) \- Опис
