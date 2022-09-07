---
navigation:
  - swoole-mysql.query.md: '« SwooleMySQL::query'
  - class.swoole-process.md: SwooleProcess »
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleMySQLException
---
# Клас SwooleMySQLException

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```synopsis



    
     
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
