Безпосередньо встановлює параметр запиту посилення (bq)

-   [« SolrDisMaxQuery::setBoostFunction](solrdismaxquery.setboostfunction.html)
    
-   [SolrDisMaxQuery::setMinimumMatch »](solrdismaxquery.setminimummatch.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Безпосередньо встановлює параметр запиту посилення (bq)
    

# SolrDisMaxQuery::setBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::setBoostQuery - Безпосередньо встановлює параметр запиту посилення (bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setBoostQuery(string $q): SolrDisMaxQuery
```

Задає параметр запиту посилення (bq).

### Список параметрів

`q`

Запит.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setBoostQuery()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");

$dismaxQuery->setBoostQuery('cat:electronics manu:local^2');
echo $dismaxQuery.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bq=cat:electronics manu:local^2
```

### Дивіться також

-   [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.html) - Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::removeBoostQuery()](solrdismaxquery.removeboostquery.html) - Видаляє часткове підвищення запиту на ім'я поля (bq)