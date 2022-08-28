Клас mysqliwarning

-   [« mysqli\_driver::$report\_mode](mysqli-driver.report-mode.html)
    
-   [mysqli\_warning::\_\_construct »](mysqli-warning.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   Клас mysqliwarning
    

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

-   [mysqli\_warning::\_\_construct](mysqli-warning.construct.html) — Закритий конструктор для заборони прямого створення екземпляра
-   [mysqli\_warning::next](mysqli-warning.next.html) — Отримує таке попередження