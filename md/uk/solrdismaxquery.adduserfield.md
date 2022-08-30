Додає поле до параметра поля користувача (uf)

-   [« SolrDisMaxQuery::addTrigramPhraseField](solrdismaxquery.addtrigramphrasefield.html)
    
-   [SolrDisMaxQuery::construct »](solrdismaxquery.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Додає поле до параметра поля користувача (uf)
    

# Solr DisMax Query::add User Field

(No version information available, might only be in Git)

SolrDisMaxQuery::addUserField — Додає поле до параметра поля користувача (uf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::addUserField(string $field): SolrDisMaxQuery
```

Додає поле до параметра поля користувача (uf)

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::add User Field()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addUserField('cat')
->addUserField('text')
->addUserField('*_dt');

echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=edismax&uf=cat text *_dt
```

### Дивіться також

-   [SolrDisMaxQuery::removeUserField()](solrdismaxquery.removeuserfield.html) - Видаляє поле з параметра користувацьких полів (uf)
-   [SolrDisMaxQuery::setUserFields()](solrdismaxquery.setuserfields.html) - Встановлює параметр полів користувача (uf)