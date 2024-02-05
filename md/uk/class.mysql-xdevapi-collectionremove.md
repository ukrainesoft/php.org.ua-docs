---
navigation:
  - mysql-xdevapi-collectionmodify.unset.md: '« CollectionModify::unset'
  - mysql-xdevapi-collectionremove.bind.md: 'CollectionRemove::bind »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас CollectionRemove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [CollectionRemove::bind](mysql-xdevapi-collectionremove.bind.md)— Прив'язує значення до заповнювача
-   [CollectionRemove::\_\_construct](mysql-xdevapi-collectionremove.construct.md) \- Конструктор класу CollectionRemove
-   [CollectionRemove::execute](mysql-xdevapi-collectionremove.execute.md) \- Виконує операцію видалення
-   [CollectionRemove::limit](mysql-xdevapi-collectionremove.limit.md)— Обмежує кількість документів для видалення
-   [CollectionRemove::sort](mysql-xdevapi-collectionremove.sort.md) \- Встановлює критерії сортування
