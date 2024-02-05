---
navigation:
  - solrquery.collapse.md: '« SolrQuery::collapse'
  - solrquery.destruct.md: 'SolrQuery::\_\_destruct »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::\_\_construct

(PECL solr >= 0.9.2)

SolrQuery::\_\_construct — Конструктор

### Опис

public **SolrQuery::\_\_construct**(string`$q`

Конструктор.

### Список параметрів

`q`

Додатковий пошуковий запит

### Значення, що повертаються

Нічого

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md)в случае передачи недопустимого параметра.

### список змін

| Версия | Опис |
| --- | --- |
| PECL solr 2.0.0 | Якщо `q` був неприпустимим, викидається виняток [SolrIllegalArgumentException](class.solrillegalargumentexception.md). . Раніше видавалась помилка. |
