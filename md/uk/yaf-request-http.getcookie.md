---
navigation:
  - yaf-request-http.get.md: '« YafRequestHttp::get'
  - yaf-request-http.getfiles.md: 'YafRequestHttp::getFiles »'
  - index.md: PHP Manual
  - class.yaf-request-http.md: YafRequestHttp
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

-   [YafRequestHttp::get()](yaf-request-http.get.md) - Отримує змінну від клієнта
-   [YafRequestHttp::getQuery()](yaf-request-http.getquery.md) - Отримує параметр запиту
-   [YafRequestHttp::getPost()](yaf-request-http.getpost.md) - Отримує змінну POST
-   [YafRequestHttp::getRaw()](yaf-request-http.getraw.md) - Отримує необроблене тіло запиту
-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.md) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.md) - Отримує параметр дзвінка
