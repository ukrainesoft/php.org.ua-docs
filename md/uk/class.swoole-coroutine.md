Клас SwooleCoroutine

-   [« SwooleConnectionIterator::valid](swoole-connection-iterator.valid.html)
    
-   [SwooleCoroutine::calluserfuncarray »](swoole-coroutine.call-user-func-array.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleCoroutine
    

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

-   [SwooleCoroutine::calluserfuncarray](swoole-coroutine.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [SwooleCoroutine::calluserfunc](swoole-coroutine.call-user-func.html) - Викликає callback-функцію, задану першим параметром
-   [SwooleCoroutine::cliwait](swoole-coroutine.cli-wait.html) - Опис
-   [SwooleCoroutine::create](swoole-coroutine.create.html) - Опис
-   [SwooleCoroutineClient::close](swoole-coroutine-client.close.html) - Опис
-   [SwooleCoroutineClient::connect](swoole-coroutine-client.connect.html) - Опис
-   [SwooleCoroutineClient::construct](swoole-coroutine-client.construct.html) - Опис
-   [SwooleCoroutineClient::destruct](swoole-coroutine-client.destruct.html) - Опис
-   [SwooleCoroutineClient::getpeername](swoole-coroutine-client.getpeername.html) - Опис
-   [SwooleCoroutineClient::getsockname](swoole-coroutine-client.getsockname.html) - Опис
-   [SwooleCoroutineClient::isConnected](swoole-coroutine-client.isconnected.html) - Опис
-   [SwooleCoroutineClient::recv](swoole-coroutine-client.recv.html) - Опис
-   [SwooleCoroutineClient::send](swoole-coroutine-client.send.html) - Опис
-   [SwooleCoroutineClient::sendfile](swoole-coroutine-client.sendfile.html) - Опис
-   [SwooleCoroutineClient::sendto](swoole-coroutine-client.sendto.html) - Опис
-   [SwooleCoroutineClient::set](swoole-coroutine-client.set.html) - Опис
-   [SwooleCoroutineHttpClient::addFile](swoole-coroutine-http-client.addfile.html) - Опис
-   [SwooleCoroutineHttpClient::close](swoole-coroutine-http-client.close.html) - Опис
-   [SwooleCoroutineHttpClient::construct](swoole-coroutine-http-client.construct.html) - Опис
-   [SwooleCoroutineHttpClient::destruct](swoole-coroutine-http-client.destruct.html) - Опис
-   [SwooleCoroutineHttpClient::execute](swoole-coroutine-http-client.execute.html) - Опис
-   [SwooleCoroutineHttpClient::get](swoole-coroutine-http-client.get.html) - Опис
-   [SwooleCoroutineHttpClient::getDefer](swoole-coroutine-http-client.getdefer.html) - Опис
-   [SwooleCoroutineHttpClient::isConnected](swoole-coroutine-http-client.isconnected.html) - Опис
-   [SwooleCoroutineHttpClient::post](swoole-coroutine-http-client.post.html) - Опис
-   [SwooleCoroutineHttpClient::recv](swoole-coroutine-http-client.recv.html) - Опис
-   [SwooleCoroutineHttpClient::set](swoole-coroutine-http-client.set.html) - Опис
-   [SwooleCoroutineHttpClient::setCookies](swoole-coroutine-http-client.setcookies.html) - Опис
-   [SwooleCoroutineHttpClient::setData](swoole-coroutine-http-client.setdata.html) - Опис
-   [SwooleCoroutineHttpClient::setDefer](swoole-coroutine-http-client.setdefer.html) - Опис
-   [SwooleCoroutineHttpClient::setHeaders](swoole-coroutine-http-client.setheaders.html) - Опис
-   [SwooleCoroutineHttpClient::setMethod](swoole-coroutine-http-client.setmethod.html) - Опис
-   [SwooleCoroutineMySQL::close](swoole-coroutine-mysql.close.html) - Опис
-   [SwooleCoroutineMySQL::connect](swoole-coroutine-mysql.connect.html) - Опис
-   [SwooleCoroutineMySQL::construct](swoole-coroutine-mysql.construct.html) - Опис
-   [SwooleCoroutineMySQL::destruct](swoole-coroutine-mysql.destruct.html) - Опис
-   [SwooleCoroutineMySQL::getDefer](swoole-coroutine-mysql.getdefer.html) - Опис
-   [SwooleCoroutineMySQL::query](swoole-coroutine-mysql.query.html) - Опис
-   [SwooleCoroutineMySQL::recv](swoole-coroutine-mysql.recv.html) - Опис
-   [SwooleCoroutineMySQL::setDefer](swoole-coroutine-mysql.setdefer.html) - Опис
-   [SwooleCoroutine::getuid](swoole-coroutine.getuid.html) - Опис
-   [SwooleCoroutine::resume](swoole-coroutine.resume.html) - Опис
-   [SwooleCoroutine::suspend](swoole-coroutine.suspend.html) - Опис