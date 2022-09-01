---
navigation:
  - yaf-request-http.get.html: '« YafRequestHttp::get'
  - yaf-request-http.getfiles.html: 'YafRequestHttp::getFiles »'
  - index.md: PHP Manual
  - class.yaf-request-http.html: YafRequestHttp
title: 'YafRequestHttp::getCookie'
---
# YafRequestHttp::getCookie

(Yaf >=1.0.0)

YafRequestHttp::getCookie — Отримує змінну Cookie

### Опис

```methodsynopsis
public Yaf_Request_Http::getCookie(string $name, string $default = ?): mixed
```

Отримує змінну Cookie

### Список параметрів

`name`

Ім'я Cookie

`default`

Якщо параметр вказано, він буде повернутий, якщо змінна не знайдена

### Значення, що повертаються

### Дивіться також

-   [YafRequestHttp::get()](yaf-request-http.get.html) - Отримує змінну від клієнта
-   [YafRequestHttp::getQuery()](yaf-request-http.getquery.html) - Отримує параметр запиту
-   [YafRequestHttp::getPost()](yaf-request-http.getpost.html) - Отримує змінну POST
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.html) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.html) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.html) - Отримує параметр дзвінка
