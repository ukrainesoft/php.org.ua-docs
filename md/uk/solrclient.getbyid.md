---
navigation:
  - solrclient.destruct.md: '« SolrClient::\_\_destruct'
  - solrclient.getbyids.md: 'SolrClient::getByIds »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::getById'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::getById

(PECL solr >= 2.2.0)

SolrClient::getById — Отримує документ для ідентифікатора. Використовує Solr Realtime Get (RTG)

### Опис

```methodsynopsis
public SolrClient::getById(string $id): SolrQueryResponse
```

Отримує документ щодо ідентифікатора. Використовує Solr Realtime Get (RTG)

### Список параметрів

`id`

ID документа

### Значення, що повертаються

[SolrQueryResponse](class.solrqueryresponse.md)

### Приклади

**Пример #1 Пример использования**SolrClient::getById()\*\*\*\*

```php
<?php

include "bootstrap.php";

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
    'path'     => SOLR_SERVER_PATH
);

$client = new SolrClient($options);
$response = $client->getById('GB18030TEST');
print_r($response->getResponse());

?>
```

Висновок наведеного прикладу буде схожим на:

```
SolrObject Object
(
    [doc] => SolrObject Object
        (
            [id] => GB18030TEST
            [name] => Array
                (
                    [0] => Test with some GB18030 encoded characters
                )

            [features] => Array
                (
                    [0] => No accents here
                    [1] => 这是一个功能
                    [2] => This is a feature (translated)
                    [3] => 这份文件是很有光泽
                    [4] => This document is very shiny (translated)
                )

            [price] => Array
                (
                    [0] => 0
                )

            [inStock] => Array
                (
                    [0] => 1
                )

            [_version_] => 1510294336239042560
        )

)
```

### Дивіться також

-   [SolrClient::getByIds()](solrclient.getbyids.md) \- Отримує документи щодо їх ідентифікаторів. Використовує Solr Realtime Get (RTG)
