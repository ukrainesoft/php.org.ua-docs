---
navigation:
  - class.datemalformedperiodstringexception.md: « DateMalformedPeriodStringException
  - book.hrtime.md: HRTime »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateMalformedStringException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateMalformedStringException

(PHP 8 >= 8.3.0)

## Вступ

Викидається при виявленні неприпустимого рядка дати/часу.

Рядок дати/часу може передаватися як значення аргументу в методи [DateTimeImmutable::\_\_construct()](datetimeimmutable.construct.md) [DateTimeImmutable::modify()](datetimeimmutable.modify.md) [DateTime::\_\_construct()](datetime.construct.md) або [DateTime::modify()](datetime.modify.md)

## Огляд класів

```classsynopsis

    
     class DateMalformedStringException
    

    
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
