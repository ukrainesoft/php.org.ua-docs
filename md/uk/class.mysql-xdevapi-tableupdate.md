Клас TableUpdate

-   [« TableSelect::where](mysql-xdevapi-tableselect.where.html)
    
-   [TableUpdate::bind »](mysql-xdevapi-tableupdate.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Mysql\_xdevapi](book.mysql-xdevapi.html)
    
-   Клас TableUpdate
    

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

-   [TableUpdate::bind](mysql-xdevapi-tableupdate.bind.html) — Прив'язує параметри запиту на оновлення
-   [TableUpdate::\_\_construct](mysql-xdevapi-tableupdate.construct.html) - Конструктор класу TableUpdate
-   [TableUpdate::execute](mysql-xdevapi-tableupdate.execute.html) — Виконує запит на оновлення
-   [TableUpdate::limit](mysql-xdevapi-tableupdate.limit.html) - Обмежує кількість рядків для оновлення
-   [TableUpdate::orderby](mysql-xdevapi-tableupdate.orderby.html) - Встановлює критерії сортування
-   [TableUpdate::set](mysql-xdevapi-tableupdate.set.html) — Додає поле для оновлення
-   [TableUpdate::where](mysql-xdevapi-tableupdate.where.html) - Встановлює фільтр пошуку