---
navigation:
  - solrdismaxquery.setqueryalt.md: '« SolrDisMaxQuery::setQueryAlt'
  - solrdismaxquery.settiebreaker.md: 'SolrDisMaxQuery::setTieBreaker »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'Solr DisMax Query::getQuery Phrase Slop'
---
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

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::getQuery Phrase Slop()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery();
$dismaxQuery->setQueryPhraseSlop(3);
echo $dismaxQuery;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
defType=edismax&qs=3
```
