---
navigation:
  - solrdismaxquery.removetrigramphrasefield.md: '« SolrDisMaxQuery::removeTrigramPhraseField'
  - solrdismaxquery.setbigramphrasefields.md: 'SolrDisMaxQuery::setBigramPhraseFields »'
  - index.md: PHP Manual
  - class.solrdismaxquery.md: SolrDisMaxQuery
title: 'SolrDisMaxQuery::removeUserField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDisMaxQuery::removeUserField

(No version information available, might only be in Git)

Solr DisMax Query::remove UserField — Видалення поля з параметра поля користувача (uf)

### Опис

```methodsynopsis
public SolrDisMaxQuery::removeUserField(string $field): SolrDisMaxQuery
```

Видаляє поле з параметра поля користувача (uf)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`field`

Ім'я поля

### Значення, що повертаються

[SolrDisMaxQuery](class.solrdismaxquery.md)

### Приклади

**Приклад #1 Приклад використання** SolrDisMaxQuery::removeUserField()\*\*\*\*

```php
<?php

$dismaxQuery = new SolrDisMaxQuery('lucene');
$dismaxQuery
->addUserField('cat')
->addUserField('text')
->addUserField('*_dt')
;
echo $dismaxQuery.PHP_EOL;

// удалить поле 'text'
$dismaxQuery
->removeUserField('text');
echo $dismaxQuery.PHP_EOL;

?>
```

Висновок наведеного прикладу буде схожим на:

```
q=lucene&defType=%s&uf=cat text *_dt
q=lucene&defType=%s&uf=cat *_dt
```

### Дивіться також

-   [SolrDisMaxQuery::addUserField()](solrdismaxquery.adduserfield.md) \- Додає поле до параметра користувача полів (uf)
-   [SolrDisMaxQuery::setUserFields()](solrdismaxquery.setuserfields.md) \- Встановлює параметр полів користувача (uf)
