---
navigation:
  - solrdismaxquery.removeboostquery.md: '« SolrDisMaxQuery::removeBoostQuery'
  - solrdismaxquery.removequeryfield.md: 'SolrDisMaxQuery::removeQueryField »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removePhraseField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::removePhraseField

(No version information available, might only be in Git)

Solr DisMax Query::remove Phrase Field — Видаляє поле фрази (параметра)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removePhraseField(string $field): SolrDisMaxQuery
```

Видаляє поле фрази (параметра), яке було раніше додано за допомогою SolrDisMaxQuery::addPhraseField

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Пример #1 Пример использования**SolrDisMaxQuery::removePhraseField()\*\*\*\*

```php
<?php
$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
    ->addPhraseField('first', 3, 1)
    ->addPhraseField('second', 4, 1)
    ->addPhraseField('cat', 55);
echo $dismaxQuery . PHP_EOL;
echo $dismaxQuery->removePhraseField('second');
?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&pf=first~1^3 second~1^4 cat^55
q=lucene&defType=edismax&pf=first~1^3 cat^55
```

### Дивіться також

-   [SolrDisMaxQuery::addPhraseField()](solrdismaxquery.addphrasefield.md) \- Додає поле фрази (параметр pf)
-   [SolrDisMaxQuery::setPhraseFields()](solrdismaxquery.setphrasefields.md) \- Встановлює поля фрази та їх посилення (і відхилення) за допомогою параметра pf2
