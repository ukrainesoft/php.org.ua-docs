---
navigation:
  - win32service.constants.serviceinfos.md: « Win32 Service informations
  - win32service.examples.md: Приклади »
  - index.md: PHP Manual
  - book.win32service.md: win32service
title: Клас Win32ServiceException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Win32ServiceException

(PECL win32service >=1.0.0)

## Вступ

Виняток замінює старий механізм, у якому значення помилки потрібно було порівнювати із константами, щоб визначити помилку. Код виключення дорівнює значенню помилки, а повідомлення про виключення ґрунтується на відповідному імені константи.

## Огляд класів

```classsynopsis



    
     
      class Win32ServiceException
     

     
      extends
       Exception
     
     {


    /* Наследуемые свойства */
    
      protected
      string
       $message = "";
private
      string
       $string = "";
protected
      int
       $code;
protected
      string
       $file = "";
protected
      int
       $line;
private
      array
       $trace = [];
private
      ?Throwable
       $previous = null;





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
