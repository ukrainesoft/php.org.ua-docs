Клас RowResult

-   [« Result::getWarningsCount](mysql-xdevapi-result.getwarningscount.html)
    
-   [RowResult::\_\_construct »](mysql-xdevapi-rowresult.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Mysql\_xdevapi](book.mysql-xdevapi.html)
    
-   Клас RowResult
    

# Клас RowResult

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\RowResult
     

     implements 
       mysql_xdevapi\BaseResult,  Traversable {


    /* Методы */
    
   public fetchAll(): array
public fetchOne(): array
public getColumnsCount(): int
public getColumnNames(): array
public getColumns(): array
public getWarnings(): array
public getWarningsCount(): int

   }
```

## Зміст

-   [RowResult::\_\_construct](mysql-xdevapi-rowresult.construct.html) - Конструктор класу RowResult
-   [RowResult::fetchAll](mysql-xdevapi-rowresult.fetchall.html) — Отримує всі рядки з результату
-   [RowResult::fetchOne](mysql-xdevapi-rowresult.fetchone.html) — Отримує рядок із результату
-   [RowResult::getColumnsCount](mysql-xdevapi-rowresult.getcolumncount.html) — Отримує кількість стовпців
-   [RowResult::getColumnNames](mysql-xdevapi-rowresult.getcolumnnames.html) — Отримує всі імена стовпців
-   [RowResult::getColumns](mysql-xdevapi-rowresult.getcolumns.html) — Отримує метадані стовпця
-   [RowResult::getWarnings](mysql-xdevapi-rowresult.getwarnings.html) — Отримує попередження останньої операції
-   [RowResult::getWarningsCount](mysql-xdevapi-rowresult.getwarningscount.html) — Отримує кількість попереджень останньої операції