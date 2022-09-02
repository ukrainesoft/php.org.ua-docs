---
navigation:
  - yaf-request-http.getpost.md: '« YafRequestHttp::getPost'
  - yaf-request-http.getraw.md: 'YafRequestHttp::getRaw »'
  - index.md: PHP Manual
  - class.yaf-request-http.md: YafRequestHttp
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

-   [YafRequestHttp::get()](yaf-request-http.get.md) - Отримує змінну від клієнта
-   [YafRequestHttp::getPost()](yaf-request-http.getpost.md) - Отримує змінну POST
-   [YafRequestHttp::getCookie()](yaf-request-http.getcookie.md) - Отримує змінну Cookie
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.md) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.md) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.md) - Отримує параметр дзвінка
