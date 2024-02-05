---
navigation:
  - solrdismaxquery.setminimummatch.md: '« SolrDisMaxQuery::setMinimumMatch'
  - solrdismaxquery.setphraseslop.md: 'SolrDisMaxQuery::setPhraseSlop »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::setPhraseFields'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::setPhraseFields

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

**Пример #1 Пример использования**SolrDisMaxQuery::setPhraseFields()\*\*\*\*

```php
<?php
$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery->setPhraseFields("cat~5.1^2 feature^4.5");
echo $dismaxQuery.PHP_EOL;
?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&pf=cat~5.1^2 feature^4.5
```

### Дивіться також

-   **SolrDisMaxQuery::addPhraseFields()**
-   [SolrDisMaxQuery::removePhraseField()](solrdismaxquery.removephrasefield.md) \- Видаляє поле фрази (параметра)
