---
navigation:
  - solrdismaxquery.settiebreaker.md: '« SolrDisMaxQuery::setTieBreaker'
  - solrdismaxquery.settrigramphraseslop.md: 'SolrDisMaxQuery::setTrigramPhraseSlop »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setTrigramPhraseFields'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::setTrigramPhraseFields()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery->setTrigramPhraseFields('cat~5.1^2 feature^4.5');
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання наведеного прикладу:

```
q=lucene&defType=edismax&pf3=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.md) \- Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::removeTrigramPhraseField()](solrdismaxquery.removetrigramphrasefield.md) \- Видаляє поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop()](solrdismaxquery.settrigramphraseslop.md) \- Встановлює коефіцієнт відхилення триграми фрази (параметр PS3)
