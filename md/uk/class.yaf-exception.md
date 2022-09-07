---
navigation:
  - yaf-session.valid.md: '« YafSession::valid'
  - yaf-exception.construct.md: 'YafException::construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafException
---
# Клас YafException

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Exception
     

     
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


    /* Методы */
    
   public __construct()

    public getPrevious(): void


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

## Зміст

-   [YafException::construct](yaf-exception.construct.md) - Конструктор класу YafException
-   [YafException::getPrevious](yaf-exception.getprevious.md) — Отримати попередній виняток
