Клас YafException

-   [« Yaf\_Session::valid](yaf-session.valid.html)
    
-   [Yaf\_Exception::\_\_construct »](yaf-exception.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafException
    

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

-   [Yaf\_Exception::\_\_construct](yaf-exception.construct.html) - Конструктор класу YafException
-   [Yaf\_Exception::getPrevious](yaf-exception.getprevious.html) — Отримати попередній виняток