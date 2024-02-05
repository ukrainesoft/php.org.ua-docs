---
navigation:
  - solrdismaxquery.addtrigramphrasefield.md: '« SolrDisMaxQuery::addTrigramPhraseField'
  - solrdismaxquery.construct.md: 'SolrDisMaxQuery::\_\_construct »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::addUserField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::addUserField

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

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::addUserField()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addUserField('cat')
->addUserField('text')
->addUserField('*_dt');

echo $dismaxQuery.PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=edismax&uf=cat text *_dt
```

### Дивіться також

-   [SolrDisMaxQuery::removeUserField()](solrdismaxquery.removeuserfield.md) \- Видаляє поле з параметра користувацьких полів (uf)
-   [SolrDisMaxQuery::setUserFields()](solrdismaxquery.setuserfields.md) \- Встановлює параметр полів користувача (uf)
