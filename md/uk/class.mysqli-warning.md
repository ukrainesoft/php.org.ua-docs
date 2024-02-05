---
navigation:
  - mysqli-driver.report-mode.md: '« mysqli\_driver::$report\_mode'
  - mysqli-warning.construct.md: 'mysqli\_warning::\_\_construct »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli\_warning
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас mysqli\_warning

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

-   [mysqli\_warning::\_\_construct](mysqli-warning.construct.md)— Закритий конструктор для заборони прямого створення екземпляра
-   [mysqli\_warning::next](mysqli-warning.next.md)— Отримує таке попередження
