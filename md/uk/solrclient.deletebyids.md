---
navigation:
  - solrclient.deletebyid.md: '« SolrClient::deleteById'
  - solrclient.deletebyqueries.md: 'SolrClient::deleteByQueries »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::deleteByIds'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::deleteByIds

(PECL solr >= 0.9.2)

SolrClient::deleteByIds — Видаляє за ідентифікаторами

### Опис

```methodsynopsis
public SolrClient::deleteByIds(array $ids): SolrUpdateResponse
```

Видаляє набір документів із зазначеним набором ідентифікаторів.

### Список параметрів

`ids`

Масив ідентифікаторів, що представляють поле uniqueKey, оголошене в схемі для кожного документа, що видаляється. Має бути фактична змінна php.

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.md) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteById()](solrclient.deletebyid.md) \- Видаляє за ідентифікатором
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.md) \- Видаляє всі документи, що відповідають заданому запиту
-   [SolrClient::deleteByQueries()](solrclient.deletebyqueries.md) \- Видаляє всі документи, що відповідають будь-якому із запитів
