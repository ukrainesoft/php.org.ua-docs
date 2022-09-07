---
navigation:
  - solrdismaxquery.setminimummatch.md: '« SolrDisMaxQuery::setMinimumMatch'
  - solrdismaxquery.setphraseslop.md: 'SolrDisMaxQuery::setPhraseSlop »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'Solr DisMax Query::set Phrase Fields'
---
# Solr DisMax Query::set Phrase Fields

(No version information available, might only be in Git)

SolrDisMaxQuery::setPhraseFields — Встановлює поля фрази та їх посилення (і відхилення) за допомогою pf2

### Опис

```methodsynopsis
public SolrDisMaxQuery::setPhraseFields(string $fields): SolrDisMaxQuery
```

Встановлює поля фрази та їх посилення (та відхилення) за допомогою параметра pf2.

### Список параметрів

`fields`

Поля, посилення (відхилення).

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set Phrase Fields()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery->setPhraseFields("cat~5.1^2 feature^4.5");
echo $dismaxQuery.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf=cat~5.1^2 feature^4.5
```

### Дивіться також

-   **Solr DisMax Query::add Phrase Fields()**
-   [SolrDisMaxQuery::removePhraseField()](solrdismaxquery.removephrasefield.md) - Видаляє поле фрази (параметра)
