---
navigation:
  - solrparams.set.md: '« SolrParams::set'
  - solrparams.tostring.md: 'SolrParams::toString »'
  - index.md: PHP Manual
  - class.solrparams.md: SolrParams
title: 'SolrParams::setParam'
---
# SolrParams::setParam

(PECL solr> = 0.9.2)

SolrParams::setParam — Встановлює параметр на вказане значення

### Опис

```methodsynopsis
public SolrParams::setParam(string $name, string $value): SolrParams
```

Встановлює для параметра запиту вказане значення. Використовується для параметрів, які можна вказати лише один раз. Наступні дзвінки з тим самим ім'ям параметра перевизначать існуюче значення

### Список параметрів

`name`

Ім'я параметра

`value`

Значення параметру

### Значення, що повертаються

Повертає екземпляр SolrParams у разі успішного виконання та **`false`** у разі зазначеного значення

### Приклади

**Приклад #1 Приклад використання **SolrParams::setParam()****

```php
<?php

$param = new SolrParams();

$param->setParam('q', 'solr')->setParam('rows', 2);

?>
```

Результатом виконання цього прикладу буде щось подібне:
