---
navigation:
  - yaf-request-http.construct.md: '« Yaf\_Request\_Http::\_\_construct'
  - yaf-request-http.getcookie.md: 'Yaf\_Request\_Http::getCookie »'
  - index.md: PHP Manual
  - class.yaf-request-http.md: Yaf\_Request\_Http
title: 'Yaf\_Request\_Http::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Http::get

(Yaf >=1.0.0)

Yaf\_Request\_Http::get — Отримує змінну від клієнта

### Опис

```methodsynopsis
public Yaf_Request_Http::get(string $name, string $default = ?): mixed
```

Получает переменную от клиента, метод будет искать`name` у параметрах запиту, якщо ім'я не знайдено, буде шукати в POST, GET, Cookie, Server

### Список параметрів

`name`

Ім'я змінної

`default`

Якщо параметр вказано, він буде повернутий, якщо змінна не знайдена

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Request\_Http::getQuery()](yaf-request-http.getquery.md) \- Отримує параметр запиту
-   [Yaf\_Request\_Http::getPost()](yaf-request-http.getpost.md) \- Отримує змінну POST
-   [Yaf\_Request\_Http::getCookie()](yaf-request-http.getcookie.md) \- Отримує змінну Cookie
-   [Yaf\_Request\_Http::getRaw()](yaf-request-http.getraw.md) \- Отримує необроблене тіло запиту
-   [Yaf\_Request\_Abstract::getServer()](yaf-request-abstract.getserver.md) \- Отримує змінну SERVER
-   [Yaf\_Request\_Abstract::getParam()](yaf-request-abstract.getparam.md) \- Отримує параметр дзвінка
