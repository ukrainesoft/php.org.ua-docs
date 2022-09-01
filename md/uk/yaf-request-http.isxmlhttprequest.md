---
navigation:
  - yaf-request-http.getrequest.html: '« YafRequestHttp::getRequest'
  - class.yaf-request-simple.html: YafRequestSimple »
  - index.md: PHP Manual
  - class.yaf-request-http.html: YafRequestHttp
title: 'YafRequestHttp::isXmlHttpRequest'
---
# YafRequestHttp::isXmlHttpRequest

(Yaf >=1.0.0)

YafRequestHttp::isXmlHttpRequest — Визначає, чи є запит Ajax-запитом

### Опис

```methodsynopsis
public Yaf_Request_Http::isXmlHttpRequest(): bool
```

Перевіряє запит, чи він є запитом Ajax.

> **Зауваження**
> 
> Метод залежить від заголовка запиту: HTTPЗREQUESTEDWITH деякі бібліотеки Javascript не встановлюють цей заголовок при виконанні запиту Ajax

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

boolean
