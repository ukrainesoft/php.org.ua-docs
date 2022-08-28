Додає поле фразової біграми (параметр pf2)

-   [« SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   [SolrDisMaxQuery::addBoostQuery »](solrdismaxquery.addboostquery.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Додає поле фразової біграми (параметр pf2)
    

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

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::addBigramPhraseField()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBigramPhraseField('cat', 2, 5.1)
    ->addBigramPhraseField('feature', 4.5)
;
echo $dismaxQuery;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf2=cat~5.1^2 feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::removeBigramPhraseField()](solrdismaxquery.removebigramphrasefield.html) - Видаляє поле біграми фрази (параметр pf2)
-   [SolrDisMaxQuery::setBigramPhraseFields()](solrdismaxquery.setbigramphrasefields.html) - Встановлює поля біграми фрази та їх посилення (і відхилення) за допомогою параметра pf2
-   [SolrDisMaxQuery::setBigramPhraseSlop()](solrdismaxquery.setbigramphraseslop.html) - Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)