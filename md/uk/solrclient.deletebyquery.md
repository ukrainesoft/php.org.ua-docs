Видаляє всі документи, що відповідають заданому запиту

-   [« SolrClient::deleteByQueries](solrclient.deletebyqueries.html)
    
-   [SolrClient::destruct »](solrclient.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
-   Видаляє всі документи, що відповідають заданому запиту
    

# SolrClient::deleteByQuery

(PECL solr> = 0.9.2)

SolrClient::deleteByQuery — Видаляє всі документи, які відповідають заданому запиту

### Опис

```methodsynopsis
public SolrClient::deleteByQuery(string $query): SolrUpdateResponse
```

Видаляє всі документи, які відповідають заданому запиту.

### Список параметрів

`query`

Запит

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.html) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrQuery::deleteByQuery()****

```php
<?php

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
);

$client = new SolrClient($options);

//Это сотрёт весь индекс
$client->deleteByQuery("*:*");
$client->commit();

?>
```

### Дивіться також

-   [SolrClient::deleteById()](solrclient.deletebyid.html) - Видаляє за ідентифікатором
-   [SolrClient::deleteByIds()](solrclient.deletebyids.html) - Видаляє за ідентифікаторами
-   [SolrClient::deleteByQueries()](solrclient.deletebyqueries.html) - Видаляє всі документи, що відповідають будь-якому із запитів