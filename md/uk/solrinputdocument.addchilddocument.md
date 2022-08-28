Додає дочірній документ для блокової індексації

-   [« SolrInputDocument](class.solrinputdocument.html)
    
-   [SolrInputDocument::addChildDocuments »](solrinputdocument.addchilddocuments.html)
    
-   [PHP Manual](index.html)
    
-   [SolrInputDocument](class.solrinputdocument.html)
    
-   Додає дочірній документ для блокової індексації
    

# SolrInputDocument::addChildDocument

(PECL solr> = 2.3.0)

SolrInputDocument::addChildDocument — Додає дочірній документ для блокової індексації

### Опис

```methodsynopsis
public SolrInputDocument::addChildDocument(SolrInputDocument $child): void
```

Додає дочірній документ для створення блоку документів із вкладеними документами.

### Список параметрів

`child`

Об'єкт [SolrInputDocument](class.solrinputdocument.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [SolrIllegalArgumentException](class.solrillegalargumentexception.html) у разі виникнення помилки.

Викидає виняток [SolrException](class.solrexception.html) у разі виникнення внутрішньої помилки.

### Приклади

**Приклад #1 Приклад використання **SolrInputDocument::addChildDocument()****

```php
<?php

include "bootstrap.php";

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
    'path'     => SOLR_SERVER_STORE_PATH,
);

$client = new SolrClient($options);

$product = new SolrInputDocument();

$product->addField('id', 'P-BLACK');
$product->addField('cat', 'tshirt');
$product->addField('cat', 'polo');
$product->addField('content_type', 'product');

$small = new SolrInputDocument();
$small->addField('id', 'TS-BLK-S');
$small->addField('content_type', 'sku');
$small->addField('size', 'S');
$small->addField('inventory', 100);

$medium = new SolrInputDocument();
$medium->addField('id', 'TS-BLK-M');
$medium->addField('content_type', 'sku');
$medium->addField('size', 'M');
$medium->addField('inventory', 200);

$large = new SolrInputDocument();
$large->addField('id', 'TS-BLK-L');
$large->addField('content_type', 'sku');
$large->addField('size', 'L');
$large->addField('inventory', 300);

// добавить дочерние документы
$product->addChildDocument($small);
$product->addChildDocument($medium);
$product->addChildDocument($large);

// добавить блок документа продукта в индекс
$updateResponse = $client->addDocument(
        $product,
        true, // перезаписать, если документ существует
        10000 // зафиксировать в течение 10 секунд
);

print_r($updateResponse->getResponse());
```

Результатом виконання цього прикладу буде щось подібне:

```
SolrObject Object
(
    [responseHeader] => SolrObject Object
        (
            [status] => 0
            [QTime] => 5
        )
)
```

### Дивіться також

-   [SolrInputDocument::addChildDocuments()](solrinputdocument.addchilddocuments.html) - Додає масив дочірніх документів
-   [SolrInputDocument::hasChildDocuments()](solrinputdocument.haschilddocuments.html) - Повертає true, якщо документ має дочірні документи
-   [SolrInputDocument::getChildDocuments()](solrinputdocument.getchilddocuments.html) - Повертає масив дочірніх документів (SolrInputDocument)
-   [SolrInputDocument::getChildDocumentsCount()](solrinputdocument.getchilddocumentscount.html) - Повертає кількість дочірніх документів