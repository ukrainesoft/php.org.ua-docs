Видаляє за ідентифікатором

-   [« SolrClient::construct](solrclient.construct.html)
    
-   [SolrClient::deleteByIds »](solrclient.deletebyids.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
-   Видаляє за ідентифікатором
    

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

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.html) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteByIds()](solrclient.deletebyids.html) - Видаляє за ідентифікаторами
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.html) - Видаляє всі документи, що відповідають заданому запиту
-   [SolrClient::deleteByQueries()](solrclient.deletebyqueries.html) - Видаляє всі документи, що відповідають будь-якому із запитів