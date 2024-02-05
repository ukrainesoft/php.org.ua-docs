---
navigation:
  - class.dateerror.md: « DateError
  - class.daterangeerror.md: DateRangeError »
  - index.md: PHP Manual
  - book.datetime.md: Дата час
title: Клас DateObjectError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DateObjectError

(PHP 8 >= 8.3.0)

## Вступ

Викидається, коли один із класів дати/часу не був правильно ініціалізований.

Оскільки класи дати/часу є остаточними, ці класи можна успадковувати. Якщо конструктор батьківського класу був викликаний, буде викинуто цей виняток. Це помилка програміста.

## Огляд класів

```classsynopsis

    
     class DateObjectError
    

    
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
-   [DateRangeError](class.daterangeerror.md)
