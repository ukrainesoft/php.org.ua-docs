Видаляє за ідентифікаторами

-   [« SolrClient::deleteById](solrclient.deletebyid.html)
    
-   [SolrClient::deleteByQueries »](solrclient.deletebyqueries.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
-   Видаляє за ідентифікаторами
    

# SolrClient::deleteByIds

(PECL solr> = 0.9.2)

SolrClient::deleteByIds — Видалити за ідентифікаторами

### Опис

```methodsynopsis
public SolrClient::deleteByIds(array $ids): SolrUpdateResponse
```

Видаляє набір документів із зазначеним набором ідентифікаторів.

### Список параметрів

`ids`

Масив ідентифікаторів, що представляють поле uniqueKey, оголошене у схемі для кожного документа, що видаляється. Має бути фактична змінна php.

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.html) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteById()](solrclient.deletebyid.html) - Видаляє за ідентифікатором
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.html) - Видаляє всі документи, що відповідають заданому запиту
-   [SolrClient::deleteByQueries()](solrclient.deletebyqueries.html) - Видаляє всі документи, що відповідають будь-якому із запитів