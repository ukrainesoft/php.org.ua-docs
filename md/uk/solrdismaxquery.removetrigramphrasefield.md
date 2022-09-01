---
navigation:
  - solrdismaxquery.removequeryfield.md: '« SolrDisMaxQuery::removeQueryField'
  - solrdismaxquery.removeuserfield.md: 'SolrDisMaxQuery::removeUserField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removeTrigramPhraseField'
---
# SolrDisMaxQuery::removeTrigramPhraseField

(No version information available, might only be in Git)

SolrDisMaxQuery::removeTrigramPhraseField — Видаляє поле триграми (параметр pf3)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeTrigramPhraseField(string $field): SolrDisMaxQuery
```

Видаляє поле триграми (параметр pf3)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::removeTrigramPhraseField()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addTrigramPhraseField('cat', 2, 5.1)
->addTrigramPhraseField('feature', 4.5)
;
echo $dismaxQuery.PHP_EOL;
// удаление
$dismaxQuery
->removeTrigramPhraseField('cat');
echo $dismaxQuery.PHP_EOL;

?>
```

Результат виконання цього прикладу:

```
q=lucene&defType=%s&pf3=cat~5.1^2 feature^4.5
q=lucene&defType=%s&pf3=feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.md) - Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.md) - Безпосередньо встановлює поля триграм фрази (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop()](solrdismaxquery.settrigramphraseslop.md) - Встановлює коефіцієнт відхилення триграми фрази (параметр PS3)
