Клас YarServerException

-   [« YarConcurrentClient::reset](yar-concurrent-client.reset.html)
    
-   [YarServerException::getType »](yar-server-exception.gettype.html)
    
-   [PHP Manual](index.md)
    
-   [Yar](book.yar.md)
    
-   Клас YarServerException
    

# Клас YarServerException

(No version information available, might only be in Git)

## Вступ

Якщо сервіс викидає винятки, на стороні клієнта буде викинуто виняток YarServerВисновок.

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

type

## Зміст

-   [YarServerException::getType](yar-server-exception.gettype.html) — Отримати тип виключення