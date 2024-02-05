---
navigation:
  - mysql-xdevapi-expression.construct.md: '« Expression::\_\_construct'
  - mysql-xdevapi-result.construct.md: 'Result::\_\_construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас Result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [Result::\_\_construct](mysql-xdevapi-result.construct.md) \- Конструктор класу Result
-   [Result::getAffectedItemsCount](mysql-xdevapi-result.getaffecteditemscount.md)— Отримує кількість порушених рядків
-   [Result::getAutoIncrementValue](mysql-xdevapi-result.getautoincrementvalue.md)— Отримує значення автоінкремента
-   [Result::getGeneratedIds](mysql-xdevapi-result.getgeneratedids.md)— Отримує згенеровані ідентифікатори
-   [Result::getWarnings](mysql-xdevapi-result.getwarnings.md)— Отримує попередження останньої операції
-   [Result::getWarningsCount](mysql-xdevapi-result.getwarningscount.md)— Отримує кількість попереджень останньої операції
