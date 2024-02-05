---
navigation:
  - mysqli-warning.next.md: '« mysqli\_warning::next'
  - mysqli-sql-exception.getsqlstate.md: 'mysqli\_sql\_exception::getSqlState »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli\_sql\_exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас mysqli\_sql\_exception

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

## Властивості

sqlstate

Код sqlstate.

## Зміст

-   [mysqli\_sql\_exception::getSqlState](mysqli-sql-exception.getsqlstate.md)— Повертає код помилки SQLSTATE
