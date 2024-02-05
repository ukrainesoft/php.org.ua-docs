---
navigation:
  - swoole-event.write.md: '« Swoole\\Event::write'
  - class.swoole-http-client.md: Swoole\\Http\\Client »
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Exception

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
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
