---
navigation:
  - mysql-xdevapi-sqlstatementresult.nextresult.html: '« SqlStatementResult::nextResult'
  - mysql-xdevapi-statement.construct.html: 'Statement::construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас Statement
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

-   [Statement::construct](mysql-xdevapi-statement.construct.html) - Опис конструктора
-   [Statement::getNextResult](mysql-xdevapi-statement.getnextresult.html) — Отримує наступний результат
-   [Statement::getResult](mysql-xdevapi-statement.getresult.html) — Отримує результат
-   [Statement::hasMoreResults](mysql-xdevapi-statement.hasmoreresults.html) — Перевіряє, чи є ще результати
