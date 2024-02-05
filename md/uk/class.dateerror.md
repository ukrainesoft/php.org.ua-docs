---
navigation:
  - timezones.others.md: « Інші
  - class.dateobjecterror.md: DateObjectError »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateError

(PHP 8 >= 8.3.0)

## Вступ

Викидається, коли база даних часових поясів не знайдена або містить неприпустимі дані (ушкоджена).

Цей виняток не викидається і не залежить від коду. Є два дочірні класи-виключення ([DateObjectError](class.dateobjecterror.md) і [DateRangeError](class.daterangeerror.md)), які викидаються при помилках програміста чи помилках у діапазонах дат.

## Огляд класів

```classsynopsis

    
     class DateError
    

    
     extends
      Error
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

-   [DateObjectError](class.dateobjecterror.md)
-   [DateRangeError](class.daterangeerror.md)
