Клас SwooleException

-   [« SwooleEvent::write](swoole-event.write.html)
    
-   [SwooleHttpClient »](class.swoole-http-client.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleException
    

# Клас SwooleException

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```synopsis



    
     
      class Swoole\Exception
     

     
      extends
       Exception
     

     implements 
       Throwable {

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


   }
```