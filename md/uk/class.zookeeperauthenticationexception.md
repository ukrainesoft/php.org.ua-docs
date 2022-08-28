Клас ZookeeperAuthenticationException

-   [« ZookeeperException](class.zookeeperexception.html)
    
-   [ZookeeperConnectionException »](class.zookeeperconnectionexception.html)
    
-   [PHP Manual](index.html)
    
-   [ZooKeeper](book.zookeeper.html)
    
-   Клас ZookeeperAuthenticationException
    

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