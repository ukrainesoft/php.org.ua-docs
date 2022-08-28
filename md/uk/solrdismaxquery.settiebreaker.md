Встановлює параметр Tie Breaker (параметр tie)

-   [« SolrDisMaxQuery::setQueryPhraseSlop](solrdismaxquery.setqueryphraseslop.html)
    
-   [SolrDisMaxQuery::setTrigramPhraseFields »](solrdismaxquery.settrigramphrasefields.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Встановлює параметр Tie Breaker (параметр tie)
    

# Solr DisMax Query::set TieBreaker

(No version information available, might only be in Git)

SolrDisMaxQuery::setTieBreaker — Встановлює параметр Tie Breaker (параметр tie)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setTieBreaker(string $tieBreaker): SolrDisMaxQuery
```

Встановлює параметр Tie Breaker (Параметр tie).

### Список параметрів

`tieBreaker`

Параметр *tie* вказує значення з плаваючою точкою (яке має бути набагато менше 1) для використання як вирішення конфліктів у запитах DisMax.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set TieBreaker()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setTieBreaker(0.1);

echo $dismaxQuery;
?>
```

Результат виконання цього прикладу:

```
defType=edismax&tie=0.1
```