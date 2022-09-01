---
navigation:
  - solrclient.commit.md: '« SolrClient::commit'
  - solrclient.deletebyid.md: 'SolrClient::deleteById »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::construct'
---
# SolrClient::construct

(PECL solr> = 0.9.2)

SolrClient::construct - Конструктор об'єкта SolrClient

### Опис

public **SolrClient::construct**(array `$clientOptions`

Конструктор об'єкта SolrClient

### Список параметрів

`clientOptions`

Масив, що містить один із таких ключів:

secure (Логічне значення, яке вказує, чи слід підключатися в безпечному режимі)

-   hostname (Ім'я хоста для сервера Solr)
-   port (Номер порту)
-   path (Шлях до Solr)
-   wt (ім'я автора відповіді, наприклад xml, json)
-   login (Ім'я користувача, яке використовується для HTTP-автентифікації, якщо є)
-   password (Пароль HTTP-автентифікації)
-   proxyhost (ім'я хоста для проксі-сервера, якщо є)
-   proxyport (Порт проксі)
-   proxylogin (Ім'я користувача проксі)
-   proxypassword (Пароль проксі)
-   timeout (Максимальний час у секундах, дозволений для операції передачі http. За замовчуванням 30 секунд)
-   sslcert (ім'я файлу у форматі PEM, що містить закритий ключ + закритий сертифікат (об'єднані в цьому порядку))
-   sslkey (Ім'я файлу лише для файлу закритого ключа у форматі PEM)
-   sslkeypassword (Пароль для закритого ключа)
-   sslcainfo (ім'я файлу, що містить один або кілька сертифікатів CA для перевірки однорангового вузла)
-   sslcapath (Ім'я каталогу, що містить кілька сертифікатів CA для перевірки однорангового вузла)

Зверніть увагу: якщо файл sslcert містить лише приватний сертифікат, вам необхідно вказати окремий файл sslkey.

Параметр sslkeypassword необхідний, якщо встановлені параметри sslcert або sslkey.

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.md) у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SolrClient::construct()****

```php
<?php

$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
    'path'     => SOLR_PATH_TO_SOLR,
    'wt'       => 'xml',
);

$client = new SolrClient($options);

$doc = new SolrInputDocument();

$doc->addField('id', 334455);
$doc->addField('cat', 'Software');
$doc->addField('cat', 'Lucene');

$updateResponse = $client->addDocument($doc);

?>
```

Результатом виконання цього прикладу буде щось подібне:

### Дивіться також

-   [SolrClient::getOptions()](solrclient.getoptions.md) - Повертає внутрішні параметри клієнта
