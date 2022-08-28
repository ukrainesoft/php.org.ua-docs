Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)

-   [« SolrDisMaxQuery::setPhraseFields](solrdismaxquery.setphrasefields.html)
    
-   [SolrDisMaxQuery::setQueryAlt »](solrdismaxquery.setqueryalt.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)
    

# Solr DisMax Query::set Phrase Slop

(No version information available, might only be in Git)

SolrDisMaxQuery::setPhraseSlop — Встановлює коефіцієнт відхилення за промовчанням для запитів фраз (параметр ps)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setPhraseSlop(string $slop): SolrDisMaxQuery
```

Встановлює коефіцієнт відхилення за замовчуванням фразових запитів, побудованих з полями "pf", "pf2" and/or "pf3" (впливає на посилення). Параметр "ps".

### Список параметрів

`slop`

Коефіцієнт відхилення за замовчуванням.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set Phrase Slop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');

$dismaxQuery->setPhraseSlop(4);
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=edismax&ps=4
```