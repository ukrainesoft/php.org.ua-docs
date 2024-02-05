---
navigation:
  - mysql-xdevapi-tabledelete.where.md: '« TableDelete::where'
  - mysql-xdevapi-tableinsert.construct.md: 'TableInsert::\_\_construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас TableInsert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас TableInsert

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

Оператор для операцій вставки таблиці.

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\TableInsert
     

     implements 
       mysql_xdevapi\Executable {


    /* Методы */
    
   public execute(): mysql_xdevapi\Result
public values(array $row_values): mysql_xdevapi\TableInsert

   }
```

## Зміст

-   [TableInsert::\_\_construct](mysql-xdevapi-tableinsert.construct.md) \- Конструктор класу TableInsert
-   [TableInsert::execute](mysql-xdevapi-tableinsert.execute.md)— Виконує запит на вставку
-   [TableInsert::values](mysql-xdevapi-tableinsert.values.md)— Додає значення вставки рядка
