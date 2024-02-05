---
navigation:
  - yar-concurrent-client.reset.md: '« Yar\_Concurrent\_Client::reset'
  - yar-server-exception.gettype.md: 'Yar\_Server\_Exception::getType »'
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Клас Yar\_Server\_Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yar\_Server\_Exception

(No version information available, might only be in Git)

## Вступ

Якщо сервіс викидає винятки, на стороні клієнта буде викинуто виняток Yar\_Server\_Exception.

## Огляд класів

```classsynopsis


    
    
     
      class Yar_Server_Exception
     

     
      extends
       Exception
     
     {
    
    /* Свойства */
    
     protected
      $_type;



    /* Методы */
    
   public getType(): string


    /* Наследуемые методы */
    final public Exception::getMessage(): string
final public Exception::getPrevious(): ?Throwable
final public Exception::getCode(): int
final public Exception::getFile(): string
final public Exception::getLine(): int
final public Exception::getTrace(): array
final public Exception::getTraceAsString(): string
public Exception::__toString(): string
private Exception::__clone(): void


   }
```

## Властивості

message

code

file

line

\_type

## Зміст

-   [Yar\_Server\_Exception::getType](yar-server-exception.gettype.md)— Отримати тип виключення
