---
navigation:
  - swoole-mysql.query.md: '« Swoole\\MySQL::query'
  - class.swoole-process.md: Swoole\\Process »
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\MySQL\\Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\MySQL\\Exception

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\MySQL\Exception
     

     
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
