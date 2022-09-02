---
navigation:
  - solrquery.collapse.md: '« SolrQuery::collapse'
  - solrquery.destruct.md: 'SolrQuery::destruct »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::construct'
---
# SolrQuery::construct

(PECL solr> = 0.9.2)

SolrQuery::construct — Конструктор

### Опис

public **SolrQuery::construct**(string `$q`

Конструктор.

### Список параметрів

`q`

Додатковий пошуковий запит

### Значення, що повертаються

Нічого

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md) у разі передачі неприпустимого параметра.

### список змін

| Версия | Описание |
| --- | --- |
| PECL solr 2.0.0 | Якщо `q` був неприпустимим, викидається виняток [SolrIllegalArgumentException](class.solrillegalargumentexception.md). Раніше видавалась помилка. |
