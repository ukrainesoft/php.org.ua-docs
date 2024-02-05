---
navigation:
  - yaf-session.valid.md: '« Yaf\_Session::valid'
  - yaf-exception.construct.md: 'Yaf\_Exception::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Exception

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

-   [Yaf\_Exception::\_\_construct](yaf-exception.construct.md) \- Конструктор класу Yaf\_Exception
-   [Yaf\_Exception::getPrevious](yaf-exception.getprevious.md)— Отримати попередній виняток
