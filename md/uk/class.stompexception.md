---
navigation:
  - stompframe.construct.md: '« StompFrame::\_\_construct'
  - stomp.getdetails.md: 'StompException::getDetails »'
  - index.md: PHP Manual
  - book.stomp.md: Stomp
title: Клас StompException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас StompException

(PECL stomp >= 0.1.0)

## Вступ

Помилка, викликана модулем Stomp. Дивіться [Винятки](language.exceptions.md) для отримання детальної інформації про винятки PHP.

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

-   [StompException::getDetails](stomp.getdetails.md)— Повертає відомості про виключення
