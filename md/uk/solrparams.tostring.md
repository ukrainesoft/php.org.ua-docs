---
navigation:
  - solrparams.setparam.md: '« SolrParams::setParam'
  - solrparams.unserialize.md: 'SolrParams::unserialize »'
  - index.md: PHP Manual
  - class.solrparams.md: SolrParams
title: 'SolrParams::toString'
---
# SolrParams::toString

(PECL solr> = 0.9.2)

SolrParams::toString — Повертає всі параметри об'єкта у вигляді пар ім'я-значення

### Опис

```methodsynopsis
final public SolrParams::toString(bool $url_encode = false): string
```

Повертає всі параметри об'єкта у вигляді пар ім'я-значення

### Список параметрів

`url_encode`

Чи слід повертати значення в URL-закодованому вигляді

### Значення, що повертаються

У разі успішного виконання повертає рядок та **`false`** у разі виникнення помилки.
