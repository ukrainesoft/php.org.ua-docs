Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)

-   [« SolrDisMaxQuery::addBigramPhraseField](solrdismaxquery.addbigramphrasefield.html)
    
-   [SolrDisMaxQuery::addPhraseField »](solrdismaxquery.addphrasefield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)
    

# SolrDisMaxQuery::addBoostQuery

(No version information available, might only be in Git)

SolrDisMaxQuery::addBoostQuery — Додає поле підвищення запиту зі значенням та необов'язковим посиленням (параметр bq)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addBoostQuery(string $field, string $value, string $boost = ?): SolrDisMaxQuery
```

Додає поле для підвищення запиту зі значенням та підвищення (Параметр bq)

### Список параметрів

`field`

`value`

`boost`

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::addBoostQuery()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBoostQuery('cat', 'clothing', 2)
    ->addBoostQuery('cat', 'electronics', 5.1)
;
echo $dismaxQuery.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&bq=cat:clothing^2 cat:electronics^5.1
```

### Дивіться також

-   [SolrDisMaxQuery::removeBoostQuery()](solrdismaxquery.removeboostquery.html) - Видаляє часткове підвищення запиту на ім'я поля (bq)
-   [SolrDisMaxQuery::setBoostQuery()](solrdismaxquery.setboostquery.html) - безпосередньо встановлює параметр запиту посилення (bq)