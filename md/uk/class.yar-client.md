Клас YarClient

-   [« Yar\_Server::handle](yar-server.handle.html)
    
-   [Yar\_Client::\_\_call »](yar-client.call.html)
    
-   [PHP Manual](index.html)
    
-   [Yar](book.yar.html)
    
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

-   [Yar\_Client::\_\_call](yar-client.call.html) - Виклик сервісу
-   [Yar\_Client::\_\_construct](yar-client.construct.html) - Конструктор YarClient
-   [Yar\_Client::setOpt](yar-client.setopt.html) — Задати контекст дзвінка