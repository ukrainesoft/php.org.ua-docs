Клас StompException

-   [« StompFrame::construct](stompframe.construct.html)
    
-   [StompException::getDetails »](stomp.getdetails.html)
    
-   [PHP Manual](index.html)
    
-   [Stomp](book.stomp.html)
    
-   Клас StompException
    

# Клас StompException

(PECL stomp >= 0.1.0)

## Вступ

Помилка, викликана модулем Stomp. Дивіться [Исключения](language.exceptions.html) для отримання детальної інформації про винятки PHP.

## Огляд класів

```classsynopsis



    
     
      class StompException
     

     
      extends
       Exception
     
     {


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


    /* Методы */
    public getDetails(): string

   }
```

## Зміст

-   [StompException::getDetails](stomp.getdetails.html) — Повертає відомості про виключення