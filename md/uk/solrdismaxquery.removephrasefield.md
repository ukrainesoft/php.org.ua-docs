Видаляє поле фрази (параметра)

-   [« SolrDisMaxQuery::removeBoostQuery](solrdismaxquery.removeboostquery.html)
    
-   [SolrDisMaxQuery::removeQueryField »](solrdismaxquery.removequeryfield.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Видаляє поле фрази (параметра)
    

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

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **SolrDisMaxQuery::removePhraseField()****

```php
<?php
$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
    ->addPhraseField('first', 3, 1)
    ->addPhraseField('second', 4, 1)
    ->addPhraseField('cat', 55);
echo $dismaxQuery . PHP_EOL;
echo $dismaxQuery->removePhraseField('second');
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&pf=first~1^3 second~1^4 cat^55
q=lucene&defType=edismax&pf=first~1^3 cat^55
```

### Дивіться також

-   [SolrDisMaxQuery::addPhraseField()](solrdismaxquery.addphrasefield.html) - Додає поле фрази (параметр pf)
-   [SolrDisMaxQuery::setPhraseFields()](solrdismaxquery.setphrasefields.html) - Встановлює поля фрази та їх посилення (і відхилення) за допомогою параметра pf2