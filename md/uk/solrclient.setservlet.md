---
navigation:
  - solrclient.setresponsewriter.html: '« SolrClient::setResponseWriter'
  - solrclient.system.html: 'SolrClient::system »'
  - index.html: PHP Manual
  - class.solrclient.html: SolrClient
title: 'SolrClient::setServlet'
---
# SolrClient::setServlet

(PECL solr> = 0.9.2)

SolrClient::setServlet — Змінює вказаний тип сервлету на нове значення

### Опис

```methodsynopsis
public SolrClient::setServlet(int $type, string $value): bool
```

Змінює вказаний тип сервлету на нове значення

### Список параметрів

`type`

Одне з наступних значень:

SolrClient::SEARCHSERVLETTYPE

-   SolrClient::UPDATESERVLETTYPE
-   SolrClient::THREADSSERVLETTYPE
-   SolrClient::PINGSERVLETTYPE
-   SolrClient::TERMSSERVLETTYPE

`value`

Нове значення для сервлету

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
