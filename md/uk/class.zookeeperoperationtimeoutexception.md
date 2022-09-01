---
navigation:
  - class.zookeepernonodeexception.html: « ZookeeperNoNodeException
  - class.zookeepersessionexception.html: ZookeeperSessionException »
  - index.html: PHP Manual
  - book.zookeeper.html: ZooKeeper
title: Клас ZookeeperOperationTimeoutException
---
# Клас ZookeeperOperationTimeoutException

(PECL zookeeper >= 0.3.0)

## Вступ

Клас обробки винятків перевищення часу очікування закінчення операції.

## Огляд класів

```classsynopsis


    
    
     
      class ZookeeperOperationTimeoutException
     
     
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
