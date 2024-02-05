---
navigation:
  - memcached.touchbykey.md: '« Memcached::touchByKey'
  - book.mqseries.md: mqseries »
  - index.md: PHP Manual
  - book.memcached.md: Memcached
title: Клас MemcachedException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
