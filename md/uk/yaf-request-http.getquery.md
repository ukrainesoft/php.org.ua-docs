---
navigation:
  - yaf-request-http.getpost.md: '« Yaf\_Request\_Http::getPost'
  - yaf-request-http.getraw.md: 'Yaf\_Request\_Http::getRaw »'
  - index.md: PHP Manual
  - class.yaf-request-http.md: Yaf\_Request\_Http
title: 'Yaf\_Request\_Http::getQuery'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Http::getQuery

(Yaf >=1.0.0)

Yaf\_Request\_Http::getQuery — Отримує параметр запиту

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

-   [Yaf\_Request\_Http::get()](yaf-request-http.get.md) \- Отримує змінну від клієнта
-   [Yaf\_Request\_Http::getPost()](yaf-request-http.getpost.md) \- Отримує змінну POST
-   [Yaf\_Request\_Http::getCookie()](yaf-request-http.getcookie.md) \- Отримує змінну Cookie
-   [Yaf\_Request\_Http::getRaw()](yaf-request-http.getraw.md) \- Отримує необроблене тіло запиту
-   [Yaf\_Request\_Abstract::getServer()](yaf-request-abstract.getserver.md) \- Отримує змінну SERVER
-   [Yaf\_Request\_Abstract::getParam()](yaf-request-abstract.getparam.md) \- Отримує параметр дзвінка
