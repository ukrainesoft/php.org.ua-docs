---
navigation:
  - yaf-request-http.construct.html: '« YafRequestHttp::construct'
  - yaf-request-http.getcookie.html: 'YafRequestHttp::getCookie »'
  - index.md: PHP Manual
  - class.yaf-request-http.html: YafRequestHttp
title: 'YafRequestHttp::get'
---
# YafRequestHttp::get

(Yaf >=1.0.0)

YafRequestHttp::get — Отримує змінну від клієнта

### Опис

```methodsynopsis
public Yaf_Request_Http::get(string $name, string $default = ?): mixed
```

Отримує змінну від клієнта, метод шукатиме `name` у параметрах запиту, якщо ім'я не знайдено, буде шукати в POST, GET, Cookie, Server

### Список параметрів

`name`

Ім'я змінної

`default`

Якщо параметр вказано, він буде повернутий, якщо змінна не знайдена

### Значення, що повертаються

### Дивіться також

-   [YafRequestHttp::getQuery()](yaf-request-http.getquery.md) - Отримує параметр запиту
-   [YafRequestHttp::getPost()](yaf-request-http.getpost.md) - Отримує змінну POST
-   [YafRequestHttp::getCookie()](yaf-request-http.getcookie.md) - Отримує змінну Cookie
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.md) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.md) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.md) - Отримує параметр дзвінка
