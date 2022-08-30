Клас mysqlisqlexception

-   [« mysqliwarning::next](mysqli-warning.next.html)
    
-   [mysqlisqlexception::getSqlState »](mysqli-sql-exception.getsqlstate.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   Клас mysqlisqlexception
    

# Клас mysqlisqlexception

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас для обробки винятків mysqli.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class mysqli_sql_exception
     

     
      extends
       RuntimeException
     
     {

    /* Свойства */
    
     protected
     string
      $sqlstate = "00000";


    /* Методы */
    
   public getSqlState(): string


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

## Властивості

sqlstate

Код sqlstate.

## Зміст

-   [mysqlisqlexception::getSqlState](mysqli-sql-exception.getsqlstate.html) — Повертає код помилки SQLSTATE