---
navigation:
  - yaf-request-abstract.getcontrollername.html: '« YafRequestAbstract::getControllerName'
  - yaf-request-abstract.getexception.html: 'YafRequestAbstract::getException »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.html: YafRequestAbstract
title: 'YafRequestAbstract::getEnv'
---
# YafRequestAbstract::getEnv

(Yaf >=1.0.0)

YafRequestAbstract::getEnv — Отримує змінну ENV

### Опис

```methodsynopsis
public Yaf_Request_Abstract::getEnv(string $name, string $default = ?): void
```

Отримує змінну ENV

### Список параметрів

`name`

Ім'я змінної

`default`

Якщо вказано цей параметр, його буде повернено, якщо змінна не знайдена

### Значення, що повертаються

Повертає рядок

### Дивіться також

-   [YafRequestAbstract::getServer()](yaf-request-abstract.getserver.html) - Отримує змінну SERVER
-   [YafRequestAbstract::getParam()](yaf-request-abstract.getparam.html) - Отримує параметр дзвінка
