---
navigation:
  - yaf-request-http.getrequest.md: '« Yaf\_Request\_Http::getRequest'
  - class.yaf-request-simple.md: Yaf\_Request\_Simple »
  - index.md: PHP Manual
  - class.yaf-request-http.md: Yaf\_Request\_Http
title: 'Yaf\_Request\_Http::isXmlHttpRequest'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Http::isXmlHttpRequest

(Yaf >=1.0.0)

Yaf\_Request\_Http::isXmlHttpRequest — Визначає, чи є запит Ajax-запитом

### Опис

```methodsynopsis
public Yaf_Request_Http::isXmlHttpRequest(): bool
```

Перевіряє запит, чи він є запитом Ajax.

> **Зауваження** :
> 
> Метод залежить від заголовка запиту: HTTP\_X\_REQUESTED\_WITH деякі бібліотеки Javascript не встановлюють цей заголовок при виконанні запиту Ajax

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

boolean
