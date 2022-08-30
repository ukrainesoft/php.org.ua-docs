Видаляє поле біграми фрази (параметр pf2)

-   [« SolrDisMaxQuery::construct](solrdismaxquery.construct.md)
    
-   [SolrDisMaxQuery::removeBoostQuery »](solrdismaxquery.removeboostquery.md)
    
-   [PHP Manual](index.md)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.md)
    
-   Видаляє поле біграми фрази (параметр pf2)
    

# SolrDisMaxQuery::removeBigramPhraseField

(No version information available, might only be in Git)

SolrDisMaxQuery::removeBigramPhraseField — Видаляє поле біграми фрази (параметр pf2)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeBigramPhraseField(string $field): SolrDisMaxQuery
```

Видаляє поле фрази біграми (параметр pf2), яке було раніше додано за допомогою [SolrDisMaxQuery::addBigramPhraseField()](solrdismaxquery.addbigramphrasefield.md)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::removeBigramPhraseField()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery("lucene");
$dismaxQuery
    ->addBigramPhraseField('cat', 2, 5.1)
    ->addBigramPhraseField('feature', 4.5)
;
echo $dismaxQuery.PHP_EOL;

// удалить cat из pf2
$dismaxQuery
    ->removeBigramPhraseField('cat');
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf2=cat~5.1^2 feature^4.5
q=lucene&defType=edismax&pf2=feature^4.5
```

### Дивіться також

-   [SolrDisMaxQuery::addBigramPhraseField()](solrdismaxquery.addbigramphrasefield.md) - Додає поле фразової біграми (параметр pf2)
-   [SolrDisMaxQuery::setBigramPhraseFields()](solrdismaxquery.setbigramphrasefields.md) - Встановлює поля біграми фрази та їх посилення (і відхилення) за допомогою параметра pf2
-   [SolrDisMaxQuery::setBigramPhraseSlop()](solrdismaxquery.setbigramphraseslop.md) - Встановлює коефіцієнт відхилення біграми фрази (параметр ps2)