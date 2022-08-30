Клас YarClient

-   [« YarServer::handle](yar-server.handle.html)
    
-   [YarClient::call »](yar-client.call.html)
    
-   [PHP Manual](index.md)
    
-   [Yar](book.yar.md)
    
-   Клас YarClient
    

# Клас YarClient

(No version information available, might only be in Git)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yar_Client
     
     {
    
    /* Свойства */
    
     protected
      $_protocol;

    protected
      $_uri;

    protected
      $_options;

    protected
      $_running;



    /* Методы */
    
   public __call(string $method, array $parameters): void
final public __construct(string $url, array $options = ?)
public setOpt(int $name, mixed $value): Yar_Client|false

   }
```

## Властивості

protocol

uri

options

running

## Зміст

-   [YarClient::call](yar-client.call.html) - Виклик сервісу
-   [YarClient::construct](yar-client.construct.html) - Конструктор YarClient
-   [YarClient::setOpt](yar-client.setopt.html) — Задати контекст дзвінка