---
navigation:
  - class.dateobjecterror.md: « DateObjectError
  - class.dateexception.md: DateException »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateRangeError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateRangeError

(PHP 8 >= 8.3.0)

## Вступ

Викидається на 32-бітових платформах методами [DateTime::getTimestamp()](datetime.gettimestamp.md) [DateTimeImmutable::getTimestamp()](datetime.gettimestamp.md) та функцією [date\_timestamp\_get()](function.date-timestamp-get.md)якщо об'єкт дати представляє дату за межами 32-бітного знакового діапазону.

## Огляд класів

```classsynopsis

    
     class DateRangeError
    

    
     extends
      DateError
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
    
   public Error::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

    final public Error::getMessage(): string
final public Error::getPrevious(): ?Throwable
final public Error::getCode(): int
final public Error::getFile(): string
final public Error::getLine(): int
final public Error::getTrace(): array
final public Error::getTraceAsString(): string
public Error::__toString(): string
private Error::__clone(): void

   }
```

## Дивіться також

-   [DateError](class.dateerror.md)
-   [DateObjectError](class.dateobjecterror.md)
