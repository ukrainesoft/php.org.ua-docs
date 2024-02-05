---
navigation:
  - class.dateexception.md: « DateException
  - class.dateinvalidtimezoneexception.md: DateInvalidTimeZoneException »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateInvalidOperationException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateInvalidOperationException

(PHP 8 >= 8.3.0)

## Вступ

Викидається методами [DateTimeImmutable::sub()](datetimeimmutable.sub.md) і [DateTime::sub()](datetime.sub.md) при спробі виконання операції, що не підтримується.

Приклад такої непідтримуваної операції - це спроба відібрати, що зберігається в об'єкті. [DateInterval](class.dateinterval.md) тимчасовий інтервал начебто `next weekday` («наступний будній день» - англ.), що представляє відносну характеристику часу, оскільки неможливо побудувати зворотне логічне твердження.

## Огляд класів

```classsynopsis

    
     class DateInvalidOperationException
    

    
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
