---
navigation:
  - solrdismaxquery.removeuserfield.md: '« SolrDisMaxQuery::removeUserField'
  - solrdismaxquery.setbigramphraseslop.md: 'SolrDisMaxQuery::setBigramPhraseSlop »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setBigramPhraseFields'
---
# SolrDisMaxQuery::setBigramPhraseFields

(No version information available, might only be in Git)

SolrDisMaxQuery::setBigramPhraseFields — Встановлює поля біграми фрази та їх посилення (і відхилення) за допомогою параметра pf2

### Опис

```methodsynopsis
public SolrDisMaxQuery::setBigramPhraseFields(string $fields): SolrDisMaxQuery
```

Встановлює поля біграми фрази та їхнього посилення (і відхилення) за допомогою параметра pf2.

### Список параметрів

`fields`

Посилення полів (відхилення).

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::setBigramPhraseFields()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery->setBigramPhraseFields("cat~5.1^2 feature^4.5");
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf2=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::setBigramPhraseSlop()](solrdismaxquery.setbigramphraseslop.md) - Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)
-   **SolrDisMaxQuery::addBigramPhraseFields()**
-   [SolrDisMaxQuery::removeBigramPhraseField()](solrdismaxquery.removebigramphrasefield.md) - Видаляє поле біграми фрази (параметр pf2)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.md) - Безпосередньо встановлює поля триграм фрази (параметр pf3)
