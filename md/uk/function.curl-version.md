---
navigation:
  - function.curl_upkeep.md: « curl\_upkeep
  - class.curlhandle.md: CurlHandle »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_version

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

curl\_version — Повертає версію cURL

### Опис

```methodsynopsis
curl_version(): array|false
```

Повертає інформацію про версію cURL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із такими елементами:

| Ключ | Опис значения |
| --- | --- |
| version\_number | 24-розрядний номер версії cURL |
| version | Номер версії cURL у вигляді рядка |
| ssl\_version\_number | 24-бітний номер версії OpenSSL |
| ssl\_version | Номер версії OpenSSL у вигляді рядка |
| libz\_version | Номер версії zlib у вигляді рядка |
| host | Інформація про хост, де була зібрана cURL |
| age |  |
| features | Битовая маска констант`CURL_VERSION_XXX` |
| protocols | Масив підтримуваних протоколів cURL |

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Необов'язковий параметр `age`видалено. |
| 7.4.0 | Необов'язковий параметр `age` оголошено застарілим; якщо передано значення, воно ігнорується. |

### Приклади

**Приклад #1 Приклад використання** curl\_version()\*\*\*\*

Цей приклад перевірить, які можливості підтримує ця збірка cURL за допомогою бітової маски. `'features'`, що повертається функцією **curl\_version()**

```php
<?php
// Получаем массив с информацией о версии curl
$version = curl_version();

// Это битовые поля, которые можно использовать
// для проверки возможностей сборки curl
$bitfields = Array(
            'CURL_VERSION_IPV6',
            'CURL_VERSION_KERBEROS4',
            'CURL_VERSION_SSL',
            'CURL_VERSION_LIBZ'
            );


foreach($bitfields as $feature)
{
    echo $feature . ($version['features'] & constant($feature) ? ' есть' : ' нет');
    echo PHP_EOL;
}
?>
```
