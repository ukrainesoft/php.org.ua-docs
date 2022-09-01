---
navigation:
  - memcached.touchbykey.html: '« Memcached::touchByKey'
  - book.mqseries.html: mqseries »
  - index.html: PHP Manual
  - book.memcached.html: Memcached
title: Клас MemcachedException
---
# Клас MemcachedException

(PECL memcached >= 0.1.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class MemcachedException
     

     
      extends
       RuntimeException
     
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
