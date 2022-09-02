---
navigation:
  - yar-server-exception.gettype.md: '« YarServerException::getType'
  - yar-client-exception.gettype.md: 'YarClientException::getType »'
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Клас YarClientException
---
# Клас YarClientException

(No version information available, might only be in Git)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yar_Client_Exception
     

     
      extends
       Exception
     
     {
    
    /* Свойства */


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

## Зміст

-   [YarClientException::getType](yar-client-exception.gettype.md) — Отримати тип виключення
