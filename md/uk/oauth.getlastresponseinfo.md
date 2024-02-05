---
navigation:
  - oauth.getlastresponseheaders.md: '« OAuth::getLastResponseHeaders'
  - oauth.getrequestheader.md: 'OAuth::getRequestHeader »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getLastResponseInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::getLastResponseInfo

(PECL OAuth >= 0.99.1)

OAuth::getLastResponseInfo — Отримати HTTP-інформацію про останню відповідь

### Опис

```methodsynopsis
public OAuth::getLastResponseInfo(): array
```

Повертає HTTP-інформацію про останню відповідь.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією на останній запит. Можна використовувати константи [curl\_getinfo()](function.curl-getinfo.md)

### Дивіться також

-   [OAuth::fetch()](oauth.fetch.md) \- Витягти захищений ресурс OAuth
-   [OAuth::getLastResponse()](oauth.getlastresponse.md) \- Отримати останню відповідь
