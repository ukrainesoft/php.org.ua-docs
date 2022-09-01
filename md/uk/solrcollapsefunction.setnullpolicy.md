---
navigation:
  - solrcollapsefunction.setmin.md: '« SolrCollapseFunction::setMin'
  - solrcollapsefunction.setsize.md: 'SolrCollapseFunction::setSize »'
  - index.md: PHP Manual
  - class.solrcollapsefunction.md: SolrCollapseFunction
title: 'SolrCollapseFunction::setNullPolicy'
---
# SolrCollapseFunction::setNullPolicy

(PECL solr> = 2.2.0)

SolrCollapseFunction::setNullPolicy — Встановлює NULL-політику

### Опис

```methodsynopsis
public SolrCollapseFunction::setNullPolicy(string $nullPolicy): SolrCollapseFunction
```

Встановлює NULL-політику. Повинна бути передана одна із трьох політик, визначених як константи класу. Приймає політики ignore (ігнорування), expand (розгортання) або collapse (згортання).

### Список параметрів

`nullPolicy`

### Значення, що повертаються

[SolrCollapseFunction](class.solrcollapsefunction.md)
