Видаляє поле з параметра поля користувача (uf)

-   [« SolrDisMaxQuery::removeTrigramPhraseField](solrdismaxquery.removetrigramphrasefield.html)
    
-   [SolrDisMaxQuery::setBigramPhraseFields »](solrdismaxquery.setbigramphrasefields.html)
    
-   [PHP Manual](index.html)
    
-   [SolrDisMaxQuery](class.solrdismaxquery.html)
    
-   Видаляє поле з параметра поля користувача (uf)
    

# Solr DisMax Query::remove User Field

(No version information available, might only be in Git)

Solr DisMax Query::remove UserField — Видалення поля з параметра поля користувача (uf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeUserField(string $field): SolrDisMaxQuery
```

Видаляє поле з параметра поля користувача (uf)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.html)

### Приклади

**Приклад #1 Приклад використання **Solr DisMax Query::remove User Field()****

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addUserField('cat')
->addUserField('text')
->addUserField('*_dt')
;
echo $dismaxQuery.PHP_EOL;

// удалить поле 'text'
$dismaxQuery
->removeUserField('text');
echo $dismaxQuery.PHP_EOL;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
q=lucene&defType=%s&uf=cat text *_dt
q=lucene&defType=%s&uf=cat *_dt
```

### Дивіться також

-   [SolrDisMaxQuery::addUserField()](solrdismaxquery.adduserfield.html) - Додає поле до параметра користувача полів (uf)
-   [SolrDisMaxQuery::setUserFields()](solrdismaxquery.setuserfields.html) - Встановлює параметр полів користувача (uf)