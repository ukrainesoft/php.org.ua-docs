---
navigation:
  - function.curl-multi-strerror.md: « curl\_multi\_strerror
  - function.curl-reset.md: curl\_reset »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_pause
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_pause

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_pause — Зупинити та відновити з'єднання

### Опис

```methodsynopsis
curl_pause(CurlHandle $handle, int $flags): int
```

Припиняє або знімає з паузи сесію cURL. Сесія може бути припинена під час виконання передачі даних у напрямку читання, запису або в обох напрямках шляхом виклику цієї функції з callback-функції, зареєстрованої за допомогою [curl\_setopt()](function.curl-setopt.md)

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

`flags`

Одна из констант\*\*`CURLPAUSE_*`\*\*

### Значення, що повертаються

Повертає один із кодів повернення (**`CURLE_OK`** якщо помилок немає).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |
