---
navigation:
  - mysql-xdevapi-tableselect.where.md: '« TableSelect::where'
  - mysql-xdevapi-tableupdate.bind.md: 'TableUpdate::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Клас TableUpdate
---
# Клас TableUpdate

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

Оператор операцій оновлення запису в таблиці.

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\TableUpdate
     

     implements 
       mysql_xdevapi\Executable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\TableUpdate
public execute(): mysql_xdevapi\TableUpdate
public limit(int $rows): mysql_xdevapi\TableUpdate
public orderby(mixed $orderby_expr, mixed ...$orderby_exprs): mysql_xdevapi\TableUpdate
public set(string $table_field, string $expression_or_literal): mysql_xdevapi\TableUpdate
public where(string $where_expr): mysql_xdevapi\TableUpdate

   }
```

## Зміст

-   [TableUpdate::bind](mysql-xdevapi-tableupdate.bind.md) — Прив'язує параметри запиту на оновлення
-   [TableUpdate::construct](mysql-xdevapi-tableupdate.construct.md) - Конструктор класу TableUpdate
-   [TableUpdate::execute](mysql-xdevapi-tableupdate.execute.md) — Виконує запит на оновлення
-   [TableUpdate::limit](mysql-xdevapi-tableupdate.limit.md) - Обмежує кількість рядків для оновлення
-   [TableUpdate::orderby](mysql-xdevapi-tableupdate.orderby.md) - Встановлює критерії сортування
-   [TableUpdate::set](mysql-xdevapi-tableupdate.set.md) — Додає поле для оновлення
-   [TableUpdate::where](mysql-xdevapi-tableupdate.where.md) - Встановлює фільтр пошуку
