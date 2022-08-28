Видаляє поле триграми (параметр pf3)

-   [« SolrDisMaxQuery::removeQueryField](solrdismaxquery.removequeryfield.html)
    
-   [SolrDisMaxQuery::removeUserField »](solrdismaxquery.removeuserfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Видаляє поле триграми (параметр pf3)
    

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

[SolrDisMaxQuery](class.solrdismaxquery.html)

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

-   [SolrDisMaxQuery::addTrigramPhraseField()](solrdismaxquery.addtrigramphrasefield.html) - Додає поле триграми (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseFields()](solrdismaxquery.settrigramphrasefields.html) - Безпосередньо встановлює поля триграм фрази (параметр pf3)
-   [SolrDisMaxQuery::setTrigramPhraseSlop()](solrdismaxquery.settrigramphraseslop.html) - Встановлює коефіцієнт відхилення триграми фрази (параметр PS3)