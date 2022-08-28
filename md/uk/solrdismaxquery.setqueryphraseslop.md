Визначає коефіцієнт відхилення, дозволений для фразових запитів, які явно включені в рядок запиту користувача (параметр qf)

-   [« SolrDisMaxQuery::setQueryAlt](solrdismaxquery.setqueryalt.html)
    
-   [SolrDisMaxQuery::setTieBreaker »](solrdismaxquery.settiebreaker.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Визначає коефіцієнт відхилення, дозволений для фразових запитів, які явно включені в рядок запиту користувача (параметр qf)
    

# Solr DisMax Query::getQuery Phrase Slop

(No version information available, might only be in Git)

SolrDisMaxQuery::setQueryPhraseSlop — Визначає коефіцієнт відхилення, дозволений для фразових запитів, явно включених до рядка запиту користувача (параметр qf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::setQueryPhraseSlop(string $slop): SolrDisMaxQuery
```

Визначає коефіцієнт відхилення, дозволений для фразових запитів, які явно включені в рядок запиту користувача (параметр *кф*

Коефіцієнт відхилення відноситься до кількості позицій, на які необхідно перемістити один токен по відношенню до іншого токену, щоб відповідати фразі, зазначеній у запиті.

### Список параметрів

`slop`

Коефіцієнт відхилення.

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::getQuery Phrase Slop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setQueryPhraseSlop(3);
echo $dismaxQuery;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=edismax&qs=3
```