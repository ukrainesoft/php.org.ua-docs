Клас CollectionFind

-   [« CollectionAdd::execute](mysql-xdevapi-collectionadd.execute.html)
    
-   [CollectionFind::bind »](mysql-xdevapi-collectionfind.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас CollectionFind
    

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

-   [CollectionFind::bind](mysql-xdevapi-collectionfind.bind.html) — Прив'язує значення до заповнювача запиту
-   [CollectionFind::construct](mysql-xdevapi-collectionfind.construct.html) - Конструктор класу CollectionFind
-   [CollectionFind::execute](mysql-xdevapi-collectionfind.execute.html) - Виконує твердження
-   [CollectionFind::fields](mysql-xdevapi-collectionfind.fields.html) — Встановлює фільтр поля документа
-   [CollectionFind::groupBy](mysql-xdevapi-collectionfind.groupby.html) - Встановлює критерії угруповання
-   [CollectionFind::having](mysql-xdevapi-collectionfind.having.html) - Встановлює умову для агрегатних функцій
-   [CollectionFind::limit](mysql-xdevapi-collectionfind.limit.html) — Обмежує кількість документів, що повертаються.
-   [CollectionFind::lockExclusive](mysql-xdevapi-collectionfind.lockexclusive.html) - Виконує операцію з EXCLUSIVE LOCK
-   [CollectionFind::lockShared](mysql-xdevapi-collectionfind.lockshared.html) - Виконує операцію з SHARED LOCK
-   [CollectionFind::offset](mysql-xdevapi-collectionfind.offset.html) — Пропускає вказану кількість елементів, що повертаються.
-   [CollectionFind::sort](mysql-xdevapi-collectionfind.sort.html) - Встановлює критерії сортування