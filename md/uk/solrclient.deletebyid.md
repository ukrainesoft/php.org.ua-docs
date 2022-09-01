---
navigation:
  - solrclient.construct.md: '« SolrClient::construct'
  - solrclient.deletebyids.md: 'SolrClient::deleteByIds »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::deleteById'
---
# SolrClient::deleteById

(PECL solr> = 0.9.2)

SolrClient::deleteById — Видаляє за ідентифікатором

### Опис

```methodsynopsis
public SolrClient::deleteById(string $id): SolrUpdateResponse
```

Видаляє документ із зазначеним ідентифікатором. Де ID - значення поля uniqueKey, оголошеного у схемі.

### Список параметрів

`id`

Значення поля uniqueKey, оголошене у схемі

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.md) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteByIds()](solrclient.deletebyids.md) - Видаляє за ідентифікаторами
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.md) - Видаляє всі документи, що відповідають заданому запиту
-   [SolrClient::deleteByQueries()](solrclient.deletebyqueries.md) - Видаляє всі документи, що відповідають будь-якому із запитів
