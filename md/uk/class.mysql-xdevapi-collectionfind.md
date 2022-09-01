---
navigation:
  - mysql-xdevapi-collectionadd.execute.html: '« CollectionAdd::execute'
  - mysql-xdevapi-collectionfind.bind.html: 'CollectionFind::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас CollectionFind
---
# Клас CollectionFind

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\CollectionFind
     

     implements 
       mysql_xdevapi\Executable,  mysql_xdevapi\CrudOperationBindable,  mysql_xdevapi\CrudOperationLimitable,  mysql_xdevapi\CrudOperationSortable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\CollectionFind
public execute(): mysql_xdevapi\DocResult
public fields(string $projection): mysql_xdevapi\CollectionFind
public groupBy(string $sort_expr): mysql_xdevapi\CollectionFind
public having(string $sort_expr): mysql_xdevapi\CollectionFind
public limit(int $rows): mysql_xdevapi\CollectionFind
public lockExclusive(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
public lockShared(int $lock_waiting_option = ?): mysql_xdevapi\CollectionFind
public offset(int $position): mysql_xdevapi\CollectionFind
public sort(string $sort_expr): mysql_xdevapi\CollectionFind

   }
```

## Зміст

-   [CollectionFind::bind](mysql-xdevapi-collectionfind.bind.md) — Прив'язує значення до заповнювача запиту
-   [CollectionFind::construct](mysql-xdevapi-collectionfind.construct.md) - Конструктор класу CollectionFind
-   [CollectionFind::execute](mysql-xdevapi-collectionfind.execute.md) - Виконує твердження
-   [CollectionFind::fields](mysql-xdevapi-collectionfind.fields.md) — Встановлює фільтр поля документа
-   [CollectionFind::groupBy](mysql-xdevapi-collectionfind.groupby.md) - Встановлює критерії угруповання
-   [CollectionFind::having](mysql-xdevapi-collectionfind.having.md) - Встановлює умову для агрегатних функцій
-   [CollectionFind::limit](mysql-xdevapi-collectionfind.limit.md) — Обмежує кількість документів, що повертаються.
-   [CollectionFind::lockExclusive](mysql-xdevapi-collectionfind.lockexclusive.md) - Виконує операцію з EXCLUSIVE LOCK
-   [CollectionFind::lockShared](mysql-xdevapi-collectionfind.lockshared.md) - Виконує операцію з SHARED LOCK
-   [CollectionFind::offset](mysql-xdevapi-collectionfind.offset.md) — Пропускає вказану кількість елементів, що повертаються.
-   [CollectionFind::sort](mysql-xdevapi-collectionfind.sort.md) - Встановлює критерії сортування
