---
navigation:
  - mysql-xdevapi-table.update.md: '« Table::update'
  - mysql-xdevapi-tabledelete.bind.md: 'TableDelete::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас TableDelete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас TableDelete

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

Оператор для операцій видалення таблиці.

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\TableDelete
     

     implements 
       mysql_xdevapi\Executable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\TableDelete
public execute(): mysql_xdevapi\Result
public limit(int $rows): mysql_xdevapi\TableDelete
public orderby(string $orderby_expr): mysql_xdevapi\TableDelete
public where(string $where_expr): mysql_xdevapi\TableDelete

   }
```

## Зміст

-   [TableDelete::bind](mysql-xdevapi-tabledelete.bind.md)— Зв'язує параметри запиту на видалення
-   [TableDelete::\_\_construct](mysql-xdevapi-tabledelete.construct.md) \- Конструктор класу TableDelete
-   [TableDelete::execute](mysql-xdevapi-tabledelete.execute.md)— Виконує запит на видалення
-   [TableDelete::limit](mysql-xdevapi-tabledelete.limit.md)— Обмежує рядки видалення
-   [TableDelete::orderby](mysql-xdevapi-tabledelete.orderby.md)— Встановлює критерії сортування видалення
-   [TableDelete::where](mysql-xdevapi-tabledelete.where.md)— Встановлює умову пошуку для видалення
