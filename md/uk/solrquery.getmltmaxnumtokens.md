---
navigation:
  - solrquery.getmltmaxnumqueryterms.md: '« SolrQuery::getMltMaxNumQueryTerms'
  - solrquery.getmltmaxwordlength.md: 'SolrQuery::getMltMaxWordLength »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getMltMaxNumTokens'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getMltMaxNumTokens

(PECL solr >= 0.9.2)

SolrQuery::getMltMaxNumTokens — Повертає максимальну кількість токенів для аналізу в кожному полі документа, яке не зберігається за допомогою TermVector

### Опис

```methodsynopsis
public SolrQuery::getMltMaxNumTokens(): int
```

Повертає максимальну кількість токенів для аналізу у кожному полі документа, яке не зберігається за допомогою TermVector.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає ціле число та **`null`**, якщо значення не встановлено.
