---
navigation:
  - solrresponse.getresponse.md: '« SolrResponse::getResponse'
  - solrresponse.success.md: 'SolrResponse::success »'
  - index.md: PHP Manual
  - class.solrresponse.md: SolrResponse
title: 'SolrResponse::setParseMode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrResponse::setParseMode

(PECL solr >= 0.9.2)

SolrResponse::setParseMode — Встановлює режим аналізу

### Опис

```methodsynopsis
public SolrResponse::setParseMode(int $parser_mode = 0): bool
```

Встановлює режим аналізу.

### Список параметрів

`parser_mode`

SolrResponse::PARSE\_SOLR\_DOC аналізує документи в екземплярах SolrDocument. SolrResponse::PARSE\_SOLR\_OBJ розбирає документ на SolrObjects.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
