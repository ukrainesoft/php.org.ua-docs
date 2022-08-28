Клас TableInsert

-   [« TableDelete::where](mysql-xdevapi-tabledelete.where.html)
    
-   [TableInsert::\_\_construct »](mysql-xdevapi-tableinsert.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Mysql\_xdevapi](book.mysql-xdevapi.html)
    
-   Клас TableInsert
    

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

-   [TableInsert::\_\_construct](mysql-xdevapi-tableinsert.construct.html) - Конструктор класу TableInsert
-   [TableInsert::execute](mysql-xdevapi-tableinsert.execute.html) — Виконує запит на вставку
-   [TableInsert::values](mysql-xdevapi-tableinsert.values.html) — Додає значення вставки рядка