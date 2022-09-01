---
navigation:
  - solrdismaxquery.setminimummatch.html: '« SolrDisMaxQuery::setMinimumMatch'
  - solrdismaxquery.setphraseslop.html: 'SolrDisMaxQuery::setPhraseSlop »'
  - index.html: PHP Manual
  - class.solrdismaxquery.html: SolrDisMaxQuery
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

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::set Phrase Fields()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery->setPhraseFields("cat~5.1^2 feature^4.5");
echo $dismaxQuery.PHP_EOL;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf=cat~5.1^2 feature^4.5
```

### Дивіться також

-   **Solr DisMax Query::add Phrase Fields()**
-   [SolrDisMaxQuery::removePhraseField()](solrdismaxquery.removephrasefield.html) - Видаляє поле фрази (параметра)
