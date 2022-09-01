---
navigation:
  - mysql-xdevapi-table.update.html: '« Table::update'
  - mysql-xdevapi-tabledelete.bind.html: 'TableDelete::bind »'
  - index.html: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас TableDelete
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

-   [TableDelete::bind](mysql-xdevapi-tabledelete.bind.html) — Зв'язує параметри запиту на видалення
-   [TableDelete::construct](mysql-xdevapi-tabledelete.construct.html) - Конструктор класу TableDelete
-   [TableDelete::execute](mysql-xdevapi-tabledelete.execute.html) — Виконує запит на видалення
-   [TableDelete::limit](mysql-xdevapi-tabledelete.limit.html) — Обмежує рядки видалення
-   [TableDelete::orderby](mysql-xdevapi-tabledelete.orderby.html) — Встановлює критерії сортування видалення
-   [TableDelete::where](mysql-xdevapi-tabledelete.where.html) — Встановлює умову пошуку для видалення
