Клас SqlStatement

-   [« Session::startTransaction](mysql-xdevapi-session.starttransaction.html)
    
-   [SqlStatement::bind »](mysql-xdevapi-sqlstatement.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас SqlStatement
    

# Клас SqlStatement

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\SqlStatement
     
     {

    /* Константы */
    
     const
     int
      EXECUTE_ASYNC = 1;

    const
     int
      BUFFERED = 2;


    /* Свойства */
    public
      $statement;



    /* Методы */
    
   public bind(string $param): mysql_xdevapi\SqlStatement
public execute(): mysql_xdevapi\Result
public getNextResult(): mysql_xdevapi\Result
public getResult(): mysql_xdevapi\Result
public hasMoreResults(): bool

   }
```

## Властивості

statement

## Обумовлені константи

**`mysql_xdevapi\SqlStatement::EXECUTE_ASYNC`**

**`mysql_xdevapi\SqlStatement::BUFFERED`**

## Зміст

-   [SqlStatement::bind](mysql-xdevapi-sqlstatement.bind.html) — Зв'язує параметри затвердження
-   [SqlStatement::construct](mysql-xdevapi-sqlstatement.construct.html) - Опис конструктора
-   [SqlStatement::execute](mysql-xdevapi-sqlstatement.execute.html) — Виконує операцію
-   [SqlStatement::getNextResult](mysql-xdevapi-sqlstatement.getnextresult.html) — Отримує наступний результат
-   [SqlStatement::getResult](mysql-xdevapi-sqlstatement.getresult.html) — Отримує результат
-   [SqlStatement::hasMoreResults](mysql-xdevapi-sqlstatement.hasmoreresults.html) — Перевіряє, чи є ще результати