---
navigation:
  - mysql-xdevapi-tabledelete.where.html: '« TableDelete::where'
  - mysql-xdevapi-tableinsert.construct.html: 'TableInsert::construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас TableInsert
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

-   [TableInsert::construct](mysql-xdevapi-tableinsert.construct.md) - Конструктор класу TableInsert
-   [TableInsert::execute](mysql-xdevapi-tableinsert.execute.md) — Виконує запит на вставку
-   [TableInsert::values](mysql-xdevapi-tableinsert.values.md) — Додає значення вставки рядка
