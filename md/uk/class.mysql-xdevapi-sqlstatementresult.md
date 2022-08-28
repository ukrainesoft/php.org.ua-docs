Клас SqlStatementResult

-   [« SqlStatement::hasMoreResults](mysql-xdevapi-sqlstatement.hasmoreresults.html)
    
-   [SqlStatementResult::\_\_construct »](mysql-xdevapi-sqlstatementresult.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Mysql\_xdevapi](book.mysql-xdevapi.html)
    
-   Клас SqlStatementResult
    

# Клас SqlStatementResult

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\SqlStatementResult
     

     implements 
       mysql_xdevapi\BaseResult,  Traversable {


    /* Методы */
    
   public fetchAll(): array
public fetchOne(): array
public getAffectedItemsCount(): int
public getColumnsCount(): int
public getColumnNames(): array
public getColumns(): Array
public getGeneratedIds(): array
public getLastInsertId(): String
public getWarnings(): array
public getWarningCounts(): int
public hasData(): bool
public nextResult(): mysql_xdevapi\Result

   }
```

## Зміст

-   [SqlStatementResult::\_\_construct](mysql-xdevapi-sqlstatementresult.construct.html) - Опис конструктора
-   [SqlStatementResult::fetchAll](mysql-xdevapi-sqlstatementresult.fetchall.html) — Отримує всі рядки з результату
-   [SqlStatementResult::fetchOne](mysql-xdevapi-sqlstatementresult.fetchone.html) — Отримує один рядок
-   [SqlStatementResult::getAffectedItemsCount](mysql-xdevapi-sqlstatementresult.getaffecteditemscount.html) — Отримує порушену кількість рядків
-   [SqlStatementResult::getColumnsCount](mysql-xdevapi-sqlstatementresult.getcolumncount.html) — Отримує кількість стовпців
-   [SqlStatementResult::getColumnNames](mysql-xdevapi-sqlstatementresult.getcolumnnames.html) — Отримує імена стовпців
-   [SqlStatementResult::getColumns](mysql-xdevapi-sqlstatementresult.getcolumns.html) — Отримує стовпці
-   [SqlStatementResult::getGeneratedIds](mysql-xdevapi-sqlstatementresult.getgeneratedids.html) — Отримує згенеровані ідентифікатори
-   [SqlStatementResult::getLastInsertId](mysql-xdevapi-sqlstatementresult.getlastinsertid.html) — Отримує останній ідентифікатор вставки
-   [SqlStatementResult::getWarnings](mysql-xdevapi-sqlstatementresult.getwarnings.html) — Отримує попередження від останньої операції
-   [SqlStatementResult::getWarningsCount](mysql-xdevapi-sqlstatementresult.getwarningcount.html) — Отримує кількість попереджень від останньої операції
-   [SqlStatementResult::hasData](mysql-xdevapi-sqlstatementresult.hasdata.html) — Перевіряє, чи є результати дані
-   [SqlStatementResult::nextResult](mysql-xdevapi-sqlstatementresult.nextresult.html) — Отримує наступний результат