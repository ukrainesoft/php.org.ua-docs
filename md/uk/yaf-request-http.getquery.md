---
navigation:
  - yaf-request-http.getpost.html: '« YafRequestHttp::getPost'
  - yaf-request-http.getraw.html: 'YafRequestHttp::getRaw »'
  - index.md: PHP Manual
  - class.yaf-request-http.html: YafRequestHttp
title: 'YafRequestHttp::getQuery'
---
# YafRequestHttp::getQuery

(Yaf >=1.0.0)

YafRequestHttp::getQuery — Отримує параметр запиту

### Опис

```methodsynopsis
public Yaf_Request_Http::getQuery(string $name, string $default = ?): mixed
```

Отримує змінну GET

### Список параметрів

`name`

Ім'я змінної

`default`

Якщо параметр вказано, він буде повернутий, якщо змінна не знайдена

### Значення, що повертаються

### Дивіться також

-   [YafRequestHttp::get()](yaf-request-http.get.html) - Отримує змінну від клієнта
-   [YafRequestHttp::getPost()](yaf-request-http.getpost.html) - Отримує змінну POST
-   [YafRequestHttp::getCookie()](yaf-request-http.getcookie.html) - Отримує змінну Cookie
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.html) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.html) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.html) - Отримує параметр дзвінка
