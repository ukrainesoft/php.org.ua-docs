---
navigation:
  - class.solrdismaxquery.md: « SolrDisMaxQuery
  - solrdismaxquery.addboostquery.md: 'SolrDisMaxQuery::addBoostQuery »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::addBigramPhraseField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::addBigramPhraseField

(No version information available, might only be in Git)

SolrDisMaxQuery::addBigramPhraseField — Додає поле фразової біграми (параметр pf2)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addBigramPhraseField(string $field, string $boost, string $slop = ?): SolrDisMaxQuery
```

Додає поле фразової біграми (параметр pf2) Вихідний формат: field~slop^boost АБО field^boost Slop не є обов'язковим

### Список параметрів

`field`

`boost`

`slop`

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::addBigramPhraseField()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBigramPhraseField('cat', 2, 5.1)
    ->addBigramPhraseField('feature', 4.5)
;
echo $dismaxQuery;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&pf2=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::removeBigramPhraseField()](solrdismaxquery.removebigramphrasefield.md) \- Видаляє поле біграми фрази (параметр pf2)
-   [SolrDisMaxQuery::setBigramPhraseFields()](solrdismaxquery.setbigramphrasefields.md) \- Встановлює поля біграми фрази та їх посилення (і відхилення) за допомогою параметра pf2
-   [SolrDisMaxQuery::setBigramPhraseSlop()](solrdismaxquery.setbigramphraseslop.md) \- Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)
