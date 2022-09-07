---
navigation:
  - function.curl-unescape.md: « curlunescape
  - class.curlhandle.md: CurlHandle »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlversion
---
# curlversion

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

curlversion — Повертає версію cURL

### Опис

```methodsynopsis
curl_version(): array|false
```

Повертає інформацію про версію cURL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із такими елементами:

| Ключ | Описание значения |
| --- | --- |
| versionnumber | 24-розрядний номер версії cURL |
| version | Номер версії cURL у вигляді рядка |
| sslversionnumber | 24-бітний номер версії OpenSSL |
| sslversion | Номер версії OpenSSL у вигляді рядка |
| libzversion | Номер версії zlib у вигляді рядка |
| host | Інформація про хост, де була зібрана cURL |
| age |  |
| features | Бітова маска констант `CURL_VERSION_XXX` |
| protocols | Масив підтримуваних протоколів cURL |

### список змін

| Версия | Описание |
| --- | --- |
|  | Необов'язковий параметр `age` видалено. |
|  | Необов'язковий параметр `age` оголошено застарілим; якщо передано значення, воно ігнорується. |

### Приклади

**Приклад #1 Приклад використання **curlversion()****

Цей приклад перевірить, які можливості підтримує ця збірка cURL за допомогою бітової маски. `'features'`, що повертається функцією **curlversion()**

```php
<?php
// Получаем Масив с информацией о версии curl
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
