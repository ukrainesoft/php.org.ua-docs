---
navigation:
  - yar-server.handle.md: '« Yar\_Server::handle'
  - yar-client.call.md: 'Yar\_Client::\_\_call »'
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Клас Yar\_Client
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yar\_Client

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

\_protocol

\_uri

\_options

\_running

## Зміст

-   [Yar\_Client::\_\_call](yar-client.call.md) \- Виклик сервісу
-   [Yar\_Client::\_\_construct](yar-client.construct.md) \- Конструктор Yar\_Client
-   [Yar\_Client::setOpt](yar-client.setopt.md)— Задає контекст дзвінка
