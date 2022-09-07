---
navigation:
  - gearmanworker.work.md: '« GearmanWorker::work'
  - book.ldap.md: LDAP »
  - index.md: PHP Manual
  - book.gearman.md: Gearman
title: Клас GearmanException
---
# Клас GearmanException

(PECL gearman >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class GearmanException
     

     
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
