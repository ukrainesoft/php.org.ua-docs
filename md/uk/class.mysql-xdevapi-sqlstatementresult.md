---
navigation:
  - mysql-xdevapi-sqlstatement.hasmoreresults.md: '« SqlStatement::hasMoreResults'
  - mysql-xdevapi-sqlstatementresult.construct.md: 'SqlStatementResult::\_\_construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас SqlStatementResult
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [SqlStatementResult::\_\_construct](mysql-xdevapi-sqlstatementresult.construct.md) \- Опис конструктора
-   [SqlStatementResult::fetchAll](mysql-xdevapi-sqlstatementresult.fetchall.md)— Отримує всі рядки з результату
-   [SqlStatementResult::fetchOne](mysql-xdevapi-sqlstatementresult.fetchone.md)— Отримує один рядок
-   [SqlStatementResult::getAffectedItemsCount](mysql-xdevapi-sqlstatementresult.getaffecteditemscount.md)— Отримує порушену кількість рядків
-   [SqlStatementResult::getColumnsCount](mysql-xdevapi-sqlstatementresult.getcolumncount.md)— Отримує кількість стовпців
-   [SqlStatementResult::getColumnNames](mysql-xdevapi-sqlstatementresult.getcolumnnames.md)— Отримує імена стовпців
-   [SqlStatementResult::getColumns](mysql-xdevapi-sqlstatementresult.getcolumns.md)— Отримує стовпці
-   [SqlStatementResult::getGeneratedIds](mysql-xdevapi-sqlstatementresult.getgeneratedids.md)— Отримує згенеровані ідентифікатори
-   [SqlStatementResult::getLastInsertId](mysql-xdevapi-sqlstatementresult.getlastinsertid.md)— Отримує останній ідентифікатор вставки
-   [SqlStatementResult::getWarnings](mysql-xdevapi-sqlstatementresult.getwarnings.md)— Отримує попередження від останньої операції
-   [SqlStatementResult::getWarningsCount](mysql-xdevapi-sqlstatementresult.getwarningcount.md)— Отримує кількість попереджень від останньої операції
-   [SqlStatementResult::hasData](mysql-xdevapi-sqlstatementresult.hasdata.md)— Перевіряє, чи є результати дані
-   [SqlStatementResult::nextResult](mysql-xdevapi-sqlstatementresult.nextresult.md)— Отримує наступний результат
