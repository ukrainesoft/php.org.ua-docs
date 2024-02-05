---
navigation:
  - class.daterangeerror.md: « DateRangeError
  - class.dateinvalidoperationexception.md: DateInvalidOperationException »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateException

(PHP 8 >= 8.3.0)

## Вступ

Батьківський клас винятків дати/часу для проблем, які виникають через помилки програміста або під час перевірки текстових аргументів вільної форми (введення користувача).

Модулем викидаються такі дочірні винятки:

-   [DateInvalidOperationException](class.dateinvalidoperationexception.md)
-   [DateInvalidTimezoneException](class.dateinvalidtimezoneexception.md)
-   [DateMalformedIntervalStringException](class.datemalformedintervalstringexception.md)
-   [DateMalformedPeriodStringException](class.datemalformedperiodstringexception.md)
-   [DateMalformedStringException](class.datemalformedstringexception.md)

## Огляд класів

```classsynopsis

    
     class DateException
    

    
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
