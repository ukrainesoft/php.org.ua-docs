---
navigation:
  - class.zookeeperexception.md: « ZookeeperException
  - class.zookeeperconnectionexception.md: ZookeeperConnectionException »
  - index.md: PHP Manual
  - book.zookeeper.md: ZooKeeper
title: Клас ZookeeperAuthenticationException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ZookeeperAuthenticationException

(PECL zookeeper >= 0.3.0)

## Вступ

Клас обробки винятків аутентифікації ZooKeeper.

## Огляд класів

```classsynopsis


    
    
     
      class ZookeeperAuthenticationException
     
     
      extends
       ZookeeperException
     
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
