---
navigation:
  - solrutils.digestxmlresponse.md: '« SolrUtils::digestXmlResponse'
  - solrutils.getsolrversion.md: 'SolrUtils::getSolrVersion »'
  - index.md: PHP Manual
  - class.solrutils.md: SolrUtils
title: 'SolrUtils::escapeQueryChars'
---
# SolrUtils::escapeQueryChars

(PECL solr> = 0.9.2)

SolrUtils::escapeQueryChars — Екранує рядок запиту Lucene

### Опис

```methodsynopsis
public static SolrUtils::escapeQueryChars(string $str): string|false
```

Lucene підтримує екранування спеціальних символів, які є частиною запиту синтаксису.

Поточний список спеціальних символів:

\- && || ! ( ) { } ^ " ~

Ці символи є частиною синтаксису запиту та мають бути екрановані

### Список параметрів

`str`

Рядок запиту, який потрібно екранувати.

### Значення, що повертаються

Повертає екранований рядок або **`false`** у разі виникнення помилки.
