---
navigation:
  - oauth.getlastresponseheaders.md: '« OAuth::getLastResponseHeaders'
  - oauth.getrequestheader.md: 'OAuth::getRequestHeader »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getLastResponseInfo'
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

Повертає масив з інформацією на останній запит. Можна використовувати константи [curlgetinfo()](function.curl-getinfo.md)

### Дивіться також

-   [OAuth::fetch()](oauth.fetch.md) - Витягти захищений ресурс OAuth
-   [OAuth::getLastResponse()](oauth.getlastresponse.md) - Отримати останню відповідь
