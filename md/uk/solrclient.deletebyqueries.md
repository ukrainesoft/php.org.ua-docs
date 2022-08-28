Видаляє всі документи, які відповідають будь-якому запиту

-   [« SolrClient::deleteByIds](solrclient.deletebyids.html)
    
-   [SolrClient::deleteByQuery »](solrclient.deletebyquery.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
-   Видаляє всі документи, які відповідають будь-якому запиту
    

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

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.

### Дивіться також

-   [SolrClient::deleteById()](solrclient.deletebyid.html) - Видаляє за ідентифікатором
-   [SolrClient::deleteByIds()](solrclient.deletebyids.html) - Видаляє за ідентифікаторами
-   [SolrClient::deleteByQuery()](solrclient.deletebyquery.html) - Видаляє всі документи, що відповідають заданому запиту