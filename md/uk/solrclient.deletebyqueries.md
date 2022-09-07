---
navigation:
  - solrclient.deletebyids.md: '« SolrClient::deleteByIds'
  - solrclient.deletebyquery.md: 'SolrClient::deleteByQuery »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::deleteByQueries'
---
# SolrClient::deleteByQueries

(PECL solr> = 0.9.2)

SolrClient::deleteByQueries — Видаляє всі документи, які відповідають будь-якому запиту.

### Опис

```methodsynopsis
public SolrClient::deleteByQueries(array $queries): SolrUpdateResponse
```

Видаляє всі документи, які відповідають будь-якому запиту

### Список параметрів

`queries`

Масив запитів. Це мусить бути фактична змінна php.

### Значення, що повертаються

Повертає SolrUpdateResponse у разі успішного виконання та викидає SolrClientException у разі виникнення помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteById()](solrclient.deletebyid.md) - Видаляє за ідентифікатором
-   [SolrClient::deleteByIds()](solrclient.deletebyids.md) - Видаляє за ідентифікаторами
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.md) - Видаляє всі документи, що відповідають заданому запиту
