---
navigation:
  - solrclient.setresponsewriter.md: '« SolrClient::setResponseWriter'
  - solrclient.system.md: 'SolrClient::system »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::setServlet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::setServlet

(PECL solr >= 0.9.2)

SolrClient::setServlet — Змінює вказаний тип сервлету на нове значення

### Опис

```methodsynopsis
public SolrClient::setServlet(int $type, string $value): bool
```

Змінює цей тип сервлета на нове значення

### Список параметрів

`type`

Одне з наступних значень:

\-SolrClient::SEARCH\_SERVLET\_TYPE

-   SolrClient::UPDATE\_SERVLET\_TYPE
-   SolrClient::THREADS\_SERVLET\_TYPE
-   SolrClient::PING\_SERVLET\_TYPE
-   SolrClient::TERMS\_SERVLET\_TYPE

`value`

Нове значення для сервлету

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
