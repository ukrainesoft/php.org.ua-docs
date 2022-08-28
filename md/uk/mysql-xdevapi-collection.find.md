Шукає документ

-   [« Collection::existsInDatabase](mysql-xdevapi-collection.existsindatabase.html)
    
-   [Collection::getName »](mysql-xdevapi-collection.getname.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\Collection](class.mysql-xdevapi-collection.html)
    
-   Шукає документ
    

# Collection::find

(No version information available, might only be in Git)

Collection::find — Шукає документ

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::find(string $search_condition = ?): mysql_xdevapi\CollectionFind
```

Шукає документ або набір документів у колекції бази даних. Знайдені документи повертаються у вигляді об'єкта CollectionFind, з якого можна витягувати результати або змінювати їх.

### Список параметрів

`search_condition`

Хоча це необов'язково, зазвичай визначається умова, що звужує результати до підмножини документів.

Умова може становити кілька елементів, синтаксис підтримує прив'язку параметрів. Вираз, який використовується як умова пошуку, повинен бути допустимим виразом SQL. Якщо умова пошуку не вказана (поле порожнє), мається на увазі find('true').

### Значення, що повертаються

Об'єкт CollectionFind для перевірки операції чи отримання знайдених документів.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::find()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

$collection->add('{"name": "Альфред",     "age": 18, "job": "Дворецкий"}')->execute();
$collection->add('{"name": "Боб",        "age": 19, "job": "Пловец"}')->execute();
$collection->add('{"name": "Фред",       "age": 20, "job": "Строитель"}')->execute();
$collection->add('{"name": "Уилма",      "age": 21, "job": "Учитель"}')->execute();
$collection->add('{"name": "Джон",       "age": 22, "job": "Учитель"}')->execute();

$find   = $collection->find('job LIKE :job AND age > :age');
$result = $find
  ->bind(['job' => 'Учитель', 'age' => 20])
  ->sort('age DESC')
  ->limit(2)
  ->execute();

print_r($result->fetchAll());
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => Array
        (
            [_id] => 00005b6b536100000000000000a8
            [age] => 22
            [job] => Учитель
            [name] => Джон
        )
    [1] => Array
        (
            [_id] => 00005b6b536100000000000000a7
            [age] => 21
            [job] => Учитель
            [name] => Уилма
        )
)
```