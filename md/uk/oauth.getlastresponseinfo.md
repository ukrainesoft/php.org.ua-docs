---
navigation:
  - oauth.getlastresponseheaders.html: '« OAuth::getLastResponseHeaders'
  - oauth.getrequestheader.html: 'OAuth::getRequestHeader »'
  - index.html: PHP Manual
  - class.oauth.html: OAuth
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

Повертає масив з інформацією на останній запит. Можна використовувати константи [curlgetinfo()](function.curl-getinfo.html)

### Дивіться також

-   [OAuth::fetch()](oauth.fetch.html) - Витягти захищений ресурс OAuth
-   [OAuth::getLastResponse()](oauth.getlastresponse.html) - Отримати останню відповідь
