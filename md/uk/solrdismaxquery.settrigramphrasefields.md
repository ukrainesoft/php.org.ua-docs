Безпосередньо встановлює поля триграми фрази (параметр pf3)

-   [« SolrDisMaxQuery::setTieBreaker](solrdismaxquery.settiebreaker.html)
    
-   [SolrDisMaxQuery::setTrigramPhraseSlop »](solrdismaxquery.settrigramphraseslop.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Безпосередньо встановлює поля триграми фрази (параметр pf3)
    

# SolrDisMaxQuery::setTrigramPhraseFields

(No version information available, might only be in Git)

SolrDisMaxQuery::setTrigramPhraseFields — Безпосередньо встановлює поля триграми фрази (параметр pf3)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTrigramPhraseFields(string $fields): SolrDisMaxQuery
```

Безпосередньо встановлює поля триграм фрази (параметр pf3).

### Список параметрів

`fields`

Полі триграми фрази.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setTrigramPhraseFields()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setTrigramPhraseFields('cat~5.1^2 feature^4.5');
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=edismax&pf3=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.html) - Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::removeTrigramPhraseField()](solrdismaxquery.removetrigramphrasefield.html) - Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop()](solrdismaxquery.settrigramphraseslop.html) - Встановлює коефіцієнт відхилення триграми фрази (параметр PS3)