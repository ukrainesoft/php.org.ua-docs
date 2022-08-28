Клас SwooleCoroutine

-   [« Swoole\\Connection\\Iterator::valid](swoole-connection-iterator.valid.html)
    
-   [Swoole\\Coroutine::call\_user\_func\_array »](swoole-coroutine.call-user-func-array.html)
    
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

-   [Swoole\\Coroutine::call\_user\_func\_array](swoole-coroutine.call-user-func-array.html) - Викликає callback-функцію з масивом параметрів
-   [Swoole\\Coroutine::call\_user\_func](swoole-coroutine.call-user-func.html) - Викликає callback-функцію, задану першим параметром
-   [Swoole\\Coroutine::cli\_wait](swoole-coroutine.cli-wait.html) - Опис
-   [Swoole\\Coroutine::create](swoole-coroutine.create.html) - Опис
-   [Swoole\\Coroutine\\Client::close](swoole-coroutine-client.close.html) - Опис
-   [Swoole\\Coroutine\\Client::connect](swoole-coroutine-client.connect.html) - Опис
-   [Swoole\\Coroutine\\Client::\_\_construct](swoole-coroutine-client.construct.html) - Опис
-   [Swoole\\Coroutine\\Client::\_\_destruct](swoole-coroutine-client.destruct.html) - Опис
-   [Swoole\\Coroutine\\Client::getpeername](swoole-coroutine-client.getpeername.html) - Опис
-   [Swoole\\Coroutine\\Client::getsockname](swoole-coroutine-client.getsockname.html) - Опис
-   [Swoole\\Coroutine\\Client::isConnected](swoole-coroutine-client.isconnected.html) - Опис
-   [Swoole\\Coroutine\\Client::recv](swoole-coroutine-client.recv.html) - Опис
-   [Swoole\\Coroutine\\Client::send](swoole-coroutine-client.send.html) - Опис
-   [Swoole\\Coroutine\\Client::sendfile](swoole-coroutine-client.sendfile.html) - Опис
-   [Swoole\\Coroutine\\Client::sendto](swoole-coroutine-client.sendto.html) - Опис
-   [Swoole\\Coroutine\\Client::set](swoole-coroutine-client.set.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::addFile](swoole-coroutine-http-client.addfile.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::close](swoole-coroutine-http-client.close.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::\_\_construct](swoole-coroutine-http-client.construct.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::\_\_destruct](swoole-coroutine-http-client.destruct.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::execute](swoole-coroutine-http-client.execute.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::get](swoole-coroutine-http-client.get.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::getDefer](swoole-coroutine-http-client.getdefer.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::isConnected](swoole-coroutine-http-client.isconnected.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::post](swoole-coroutine-http-client.post.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::recv](swoole-coroutine-http-client.recv.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::set](swoole-coroutine-http-client.set.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::setCookies](swoole-coroutine-http-client.setcookies.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::setData](swoole-coroutine-http-client.setdata.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::setDefer](swoole-coroutine-http-client.setdefer.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::setHeaders](swoole-coroutine-http-client.setheaders.html) - Опис
-   [Swoole\\Coroutine\\Http\\Client::setMethod](swoole-coroutine-http-client.setmethod.html) - Опис
-   [Swoole\\Coroutine\\MySQL::close](swoole-coroutine-mysql.close.html) - Опис
-   [Swoole\\Coroutine\\MySQL::connect](swoole-coroutine-mysql.connect.html) - Опис
-   [Swoole\\Coroutine\\MySQL::\_\_construct](swoole-coroutine-mysql.construct.html) - Опис
-   [Swoole\\Coroutine\\MySQL::\_\_destruct](swoole-coroutine-mysql.destruct.html) - Опис
-   [Swoole\\Coroutine\\MySQL::getDefer](swoole-coroutine-mysql.getdefer.html) - Опис
-   [Swoole\\Coroutine\\MySQL::query](swoole-coroutine-mysql.query.html) - Опис
-   [Swoole\\Coroutine\\MySQL::recv](swoole-coroutine-mysql.recv.html) - Опис
-   [Swoole\\Coroutine\\MySQL::setDefer](swoole-coroutine-mysql.setdefer.html) - Опис
-   [Swoole\\Coroutine::getuid](swoole-coroutine.getuid.html) - Опис
-   [Swoole\\Coroutine::resume](swoole-coroutine.resume.html) - Опис
-   [Swoole\\Coroutine::suspend](swoole-coroutine.suspend.html) - Опис