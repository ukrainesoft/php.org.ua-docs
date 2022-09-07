---
navigation:
  - mysql-xdevapi-tableinsert.values.md: '« TableInsert::values'
  - mysql-xdevapi-tableselect.bind.md: 'TableSelect::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysqlxdevapi
title: Клас TableSelect
---
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

-   [TableSelect::bind](mysql-xdevapi-tableselect.bind.md) — Прив'язує параметри запиту вибірки
-   [TableSelect::construct](mysql-xdevapi-tableselect.construct.md) - Конструктор класу TableSelect
-   [TableSelect::execute](mysql-xdevapi-tableselect.execute.md) — Виконує оператор вибірки
-   [TableSelect::groupBy](mysql-xdevapi-tableselect.groupby.md) — Встановлює критерії угруповання вибірки
-   [TableSelect::having](mysql-xdevapi-tableselect.having.md) — Встановлює вибір із умовою
-   [TableSelect::limit](mysql-xdevapi-tableselect.limit.md) — Обмежує вибрані рядки
-   [TableSelect::lockExclusive](mysql-xdevapi-tableselect.lockexclusive.md) - Виконує EXCLUSIVE LOCK
-   [TableSelect::lockShared](mysql-xdevapi-tableselect.lockshared.md) - Виконує SHARED LOCK
-   [TableSelect::offset](mysql-xdevapi-tableselect.offset.md) - Встановлює межу зміщення
-   [TableSelect::orderby](mysql-xdevapi-tableselect.orderby.md) — Встановлює критерії сортування вибірки
-   [TableSelect::where](mysql-xdevapi-tableselect.where.md) — Встановлює умову пошуку вибірки
