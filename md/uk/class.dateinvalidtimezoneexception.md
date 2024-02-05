---
navigation:
  - class.dateinvalidoperationexception.md: « DateInvalidOperationException
  - class.datemalformedintervalstringexception.md: DateMalformedIntervalStringException »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateInvalidTimeZoneException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateInvalidTimeZoneException

(PHP 8 >= 8.3.0)

## Вступ

Викидається під час передачі у метод [DateTimeZone::\_\_construct()](datetimezone.construct.md) неправильного значення.

## Огляд класів

```classsynopsis

    
     class DateInvalidTimeZoneException
    

    
     extends
      DateException
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
    
   public Exception::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

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
