---
navigation:
  - mysqli-driver.report-mode.html: '« mysqlidriver::$reportmode'
  - mysqli-warning.construct.html: 'mysqliwarning::construct »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqliwarning
---
# Клас mysqliwarning

(PHP 5, PHP 7, PHP 8)

## Вступ

Попереджає MySQL.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class mysqli_warning
     
     {

    /* Свойства */
    
     public
     string
      $message;

    public
     string
      $sqlstate;

    public
     int
      $errno;


    /* Методы */
    
   private __construct()

    public next(): bool

   }
```

## Властивості

message

Рядок повідомлення

sqlstate

Код SQLstate

errno

Номер помилки

## Зміст

-   [mysqliwarning::construct](mysqli-warning.construct.html) — Закритий конструктор для заборони прямого створення екземпляра
-   [mysqliwarning::next](mysqli-warning.next.html) — Отримує таке попередження
