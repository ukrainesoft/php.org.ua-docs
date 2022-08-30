Клас Result

-   [« Expression::construct](mysql-xdevapi-expression.construct.html)
    
-   [Result::construct »](mysql-xdevapi-result.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас Result
    

# Клас Result

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Result
     

     implements 
       mysql_xdevapi\BaseResult,  Traversable {


    /* Методы */
    
   public getAffectedItemsCount(): int
public getAutoIncrementValue(): int
public getGeneratedIds(): array
public getWarnings(): array
public getWarningsCount(): int

   }
```

## Зміст

-   [Result::construct](mysql-xdevapi-result.construct.html) - Конструктор класу Result
-   [Result::getAffectedItemsCount](mysql-xdevapi-result.getaffecteditemscount.html) — Отримує кількість порушених рядків
-   [Result::getAutoIncrementValue](mysql-xdevapi-result.getautoincrementvalue.html) — Отримує значення автоінкремента
-   [Result::getGeneratedIds](mysql-xdevapi-result.getgeneratedids.html) — Отримує згенеровані ідентифікатори
-   [Result::getWarnings](mysql-xdevapi-result.getwarnings.html) — Отримує попередження останньої операції
-   [Result::getWarningsCount](mysql-xdevapi-result.getwarningscount.html) — Отримує кількість попереджень останньої операції