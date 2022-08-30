Клас TableSelect

-   [« TableInsert::values](mysql-xdevapi-tableinsert.values.html)
    
-   [TableSelect::bind »](mysql-xdevapi-tableselect.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас TableSelect
    

# Клас TableSelect

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

Оператор для пошуку запису в таблиці.

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\TableSelect
     

     implements 
       mysql_xdevapi\Executable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\TableSelect
public execute(): mysql_xdevapi\RowResult
public groupBy(mixed $sort_expr): mysql_xdevapi\TableSelect
public having(string $sort_expr): mysql_xdevapi\TableSelect
public limit(int $rows): mysql_xdevapi\TableSelect
public lockExclusive(int $lock_waiting_option = ?): mysql_xdevapi\TableSelect
public lockShared(int $lock_waiting_option = ?): mysql_xdevapi\TableSelect
public offset(int $position): mysql_xdevapi\TableSelect
public orderby(mixed $sort_expr, mixed ...$sort_exprs): mysql_xdevapi\TableSelect
public where(string $where_expr): mysql_xdevapi\TableSelect

   }
```

## Зміст

-   [TableSelect::bind](mysql-xdevapi-tableselect.bind.html) — Прив'язує параметри запиту вибірки
-   [TableSelect::construct](mysql-xdevapi-tableselect.construct.html) - Конструктор класу TableSelect
-   [TableSelect::execute](mysql-xdevapi-tableselect.execute.html) — Виконує оператор вибірки
-   [TableSelect::groupBy](mysql-xdevapi-tableselect.groupby.html) — Встановлює критерії угруповання вибірки
-   [TableSelect::having](mysql-xdevapi-tableselect.having.html) — Встановлює вибір із умовою
-   [TableSelect::limit](mysql-xdevapi-tableselect.limit.html) — Обмежує вибрані рядки
-   [TableSelect::lockExclusive](mysql-xdevapi-tableselect.lockexclusive.html) - Виконує EXCLUSIVE LOCK
-   [TableSelect::lockShared](mysql-xdevapi-tableselect.lockshared.html) - Виконує SHARED LOCK
-   [TableSelect::offset](mysql-xdevapi-tableselect.offset.html) - Встановлює межу зміщення
-   [TableSelect::orderby](mysql-xdevapi-tableselect.orderby.html) — Встановлює критерії сортування вибірки
-   [TableSelect::where](mysql-xdevapi-tableselect.where.html) — Встановлює умову пошуку вибірки