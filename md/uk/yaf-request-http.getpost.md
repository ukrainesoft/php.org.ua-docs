---
navigation:
  - yaf-request-http.getfiles.html: '« YafRequestHttp::getFiles'
  - yaf-request-http.getquery.html: 'YafRequestHttp::getQuery »'
  - index.md: PHP Manual
  - class.yaf-request-http.html: YafRequestHttp
title: 'YafRequestHttp::getPost'
---
# YafRequestHttp::getPost

(Yaf >=1.0.0)

YafRequestHttp::getPost — Отримує змінну POST

### Опис

```methodsynopsis
public Yaf_Request_Http::getPost(string $name, string $default = ?): mixed
```

Отримує змінну POST

### Список параметрів

`name`

Ім'я змінної

`default`

Якщо параметр вказано, він буде повернутий, якщо змінна не знайдена

### Значення, що повертаються

### Дивіться також

-   [YafRequestHttp::get()](yaf-request-http.get.md) - Отримує змінну від клієнта
-   [YafRequestHttp::getQuery()](yaf-request-http.getquery.md) - Отримує параметр запиту
-   [YafRequestHttp::getCookie()](yaf-request-http.getcookie.md) - Отримує змінну Cookie
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.md) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.md) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.md) - Отримує параметр дзвінка
