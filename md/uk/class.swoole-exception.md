---
navigation:
  - swoole-event.write.md: '« SwooleEvent::write'
  - class.swoole-http-client.md: SwooleHttpClient »
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleException
---
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
