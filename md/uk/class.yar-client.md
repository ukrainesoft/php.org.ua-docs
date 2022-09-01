---
navigation:
  - yar-server.handle.html: '« YarServer::handle'
  - yar-client.call.html: 'YarClient::call »'
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Клас YarClient
---
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

-   [YarClient::call](yar-client.call.md) - Виклик сервісу
-   [YarClient::construct](yar-client.construct.md) - Конструктор YarClient
-   [YarClient::setOpt](yar-client.setopt.md) — Задати контекст дзвінка
