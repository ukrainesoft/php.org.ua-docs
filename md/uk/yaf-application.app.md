---
navigation:
  - class.yaf-application.md: « Yaf\_Application
  - yaf-application.bootstrap.md: 'Yaf\_Application::bootstrap »'
  - index.md: PHP Manual
  - class.yaf-application.md: Yaf\_Application
title: 'Yaf\_Application::app'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Application::app

(Yaf >=1.0.0)

Yaf\_Application::app — Вийняти екземпляр програми

### Опис

```methodsynopsis
public staticYaf_Application::app(): mixed
```

Витягує екземпляр класу [Yaf\_Application](class.yaf-application.md). Також для цього ви можете використати [Yaf\_Dispatcher::getApplication()](yaf-dispatcher.getapplication.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Примірник класу Yaf\_Application, якщо жодного Yaf\_Application ще не ініціалізовано, буде повернутий **`null`**

### Дивіться також

-   [Yaf\_Dispatcher::getApplication()](yaf-dispatcher.getapplication.md) \- Отримує додаток
