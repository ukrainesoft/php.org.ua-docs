---
navigation:
  - solrclient.commit.md: '« SolrClient::commit'
  - solrclient.deletebyid.md: 'SolrClient::deleteById »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClient::\_\_construct

(PECL solr >= 0.9.2)

SolrClient::\_\_construct - Конструктор об'єкта SolrClient

### Опис

public**SolrClient::\_\_construct**(array`$clientOptions`) .

Конструктор об'єкта SolrClient

### Список параметрів

`clientOptions`

Масив, що містить один із таких ключів:

\- secure (Логічне значення, яке вказує, чи слід підключатися в безпечному режимі)

-   hostname (Ім'я хоста для сервера Solr)
-   port (Номер порту)
-   path (Шлях до Solr)
-   wt (ім'я автора відповіді, наприклад xml, json)
-   login (Ім'я користувача, яке використовується для HTTP-автентифікації, якщо є)
-   password (Пароль HTTP-автентифікації)
-   proxy\_host (ім'я хоста для проксі-сервера, якщо є)
-   proxy\_port (Порт проксі)
-   proxy\_login (Ім'я користувача проксі)
-   proxy\_password (Пароль проксі)
-   timeout (Максимальний час у секундах, дозволений для операції передачі http. За замовчуванням 30 секунд)
-   ssl\_cert (ім'я файлу у форматі PEM, що містить закритий ключ + закритий сертифікат (об'єднані в цьому порядку))
-   ssl\_key (Ім'я файлу лише для файлу закритого ключа у форматі PEM)
-   ssl\_keypassword (Пароль для закритого ключа)
-   ssl\_cainfo (Ім'я файлу, що містить один або кілька сертифікатів CA для перевірки однорангового вузла)
-   ssl\_capath (Ім'я каталогу, що містить кілька сертифікатів CA для перевірки однорангового вузла)

Обратите внимание: если файл ssl\_cert містить лише приватний сертифікат, вам необхідно вказати окремий файл ssl\_key.

Параметр ssl\_keypassword необхідний, якщо встановлені параметри ssl\_cert або ssl\_key.

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md)в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SolrClient::\_\_construct()\*\*\*\*

```php
<?php

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
    'path'     => SOLR_PATH_TO_SOLR,
    'wt'       => 'xml',
);

$client = new SolrClient($options);

$doc = new SolrInputDocument();

$doc->addField('id', 334455);
$doc->addField('cat', 'Software');
$doc->addField('cat', 'Lucene');

$updateResponse = $client->addDocument($doc);

?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [SolrClient::getOptions()](solrclient.getoptions.md) \- Повертає внутрішні параметри клієнта
