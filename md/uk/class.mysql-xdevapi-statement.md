---
navigation:
  - mysql-xdevapi-sqlstatementresult.nextresult.md: '« SqlStatementResult::nextResult'
  - mysql-xdevapi-statement.construct.md: 'Statement::\_\_construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас Statement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Statement

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Statement
     
     {

    /* Константы */
    
     const
     int
      EXECUTE_ASYNC = 1;

    const
     int
      BUFFERED = 2;


    /* Методы */
    
   public getNextResult(): mysql_xdevapi\Result
public getResult(): mysql_xdevapi\Result
public hasMoreResults(): bool

   }
```

## Обумовлені константи

**`mysql_xdevapi\Statement::EXECUTE_ASYNC`**

**`mysql_xdevapi\Statement::BUFFERED`**

## Зміст

-   [Statement::\_\_construct](mysql-xdevapi-statement.construct.md) \- Опис конструктора
-   [Statement::getNextResult](mysql-xdevapi-statement.getnextresult.md)— Отримує наступний результат
-   [Statement::getResult](mysql-xdevapi-statement.getresult.md)— Отримує результат
-   [Statement::hasMoreResults](mysql-xdevapi-statement.hasmoreresults.md)— Перевіряє, чи є ще результати
