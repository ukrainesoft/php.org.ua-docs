Видаляє часткове підвищення запиту на ім'я поля (bq)

-   [« SolrDisMaxQuery::removeBigramPhraseField](solrdismaxquery.removebigramphrasefield.html)
    
-   [SolrDisMaxQuery::removePhraseField »](solrdismaxquery.removephrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Видаляє часткове підвищення запиту на ім'я поля (bq)
    

# SolrDisMaxQuery::removeBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::removeBoostQuery — Видаляє часткове підвищення запиту на ім'я поля (bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeBoostQuery(string $field): SolrDisMaxQuery
```

Видаляє частковий запит на підвищення з існуючого запиту, тільки якщо було виконано [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.html)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::removeBoostQuery()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBoostQuery('cat', 'electronics', 5.1)
    ->addBoostQuery('cat', 'hard drive')
;
echo $dismaxQuery.PHP_EOL;
// теперь удалите часть запроса с полем 'cat'
$dismaxQuery
->removeBoostQuery('cat');
echo $dismaxQuery . PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bq=cat:electronics^5.1 cat:hard drive
q=lucene&defType=edismax&bq=cat:hard drive
```

### Дивіться також

-   [SolrDisMaxQuery::addBoostQuery()](solrdismaxquery.addboostquery.html) - Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
-   [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.html) - безпосередньо встановлює параметр запиту посилення (bq)