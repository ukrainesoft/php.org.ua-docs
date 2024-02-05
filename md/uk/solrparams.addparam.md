---
navigation:
  - solrparams.add.md: '« SolrParams::add'
  - solrparams.get.md: 'SolrParams::get »'
  - index.md: PHP Manual
  - class.solrparams.md: SolrParams
title: 'SolrParams::addParam'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrParams::addParam

(PECL solr >= 0.9.2)

SolrParams::addParam — Додає параметр до об'єкта

### Опис

```methodsynopsis
public SolrParams::addParam(string $name, string $value): SolrParams
```

Додавання параметра до об'єкта. Використовується для параметрів, які можна вказувати кілька разів.

### Список параметрів

`name`

Ім'я параметра

`value`

Значення параметра

### Значення, що повертаються

У разі успішного виконання повертає об'єкт SolrParam та \*\*`false`\*\*в случае возникновения ошибки.
