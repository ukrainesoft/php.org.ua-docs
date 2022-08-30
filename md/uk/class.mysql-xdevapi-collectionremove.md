Клас CollectionRemove

-   [« CollectionModify::unset](mysql-xdevapi-collectionmodify.unset.html)
    
-   [CollectionRemove::bind »](mysql-xdevapi-collectionremove.bind.html)
    
-   [PHP Manual](index.md)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Клас CollectionRemove
    

# Клас CollectionRemove

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\CollectionRemove
     

     implements 
       mysql_xdevapi\Executable,  mysql_xdevapi\CrudOperationBindable,  mysql_xdevapi\CrudOperationLimitable,  mysql_xdevapi\CrudOperationSortable {


    /* Методы */
    
   public bind(array $placeholder_values): mysql_xdevapi\CollectionRemove
public execute(): mysql_xdevapi\Result
public limit(int $rows): mysql_xdevapi\CollectionRemove
public sort(string $sort_expr): mysql_xdevapi\CollectionRemove

   }
```

## Зміст

-   [CollectionRemove::bind](mysql-xdevapi-collectionremove.bind.html) — Прив'язує значення до заповнювача
-   [CollectionRemove::construct](mysql-xdevapi-collectionremove.construct.html) - Конструктор класу CollectionRemove
-   [CollectionRemove::execute](mysql-xdevapi-collectionremove.execute.html) - Виконує операцію видалення
-   [CollectionRemove::limit](mysql-xdevapi-collectionremove.limit.html) — Обмежує кількість документів для видалення
-   [CollectionRemove::sort](mysql-xdevapi-collectionremove.sort.html) - Встановлює критерії сортування