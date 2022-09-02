---
navigation:
  - class.yaf-application.md: « YafApplication
  - yaf-application.bootstrap.md: 'YafApplication::bootstrap »'
  - index.md: PHP Manual
  - class.yaf-application.md: YafApplication
title: 'YafApplication::app'
---
# YafApplication::app

(Yaf >=1.0.0)

YafApplication::app — Вийняти екземпляр програми

### Опис

```methodsynopsis
public staticYaf_Application::app(): mixed
```

Витягує екземпляр класу [YafApplication](class.yaf-application.md). Також для цього ви можете використати [YafDispatcher::getApplication()](yaf-dispatcher.getapplication.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Примірник класу YafApplication, якщо жодного YafApplication ще не ініціалізовано, буде повернутий **`null`**

### Дивіться також

-   [YafDispatcher::getApplication()](yaf-dispatcher.getapplication.md) - Отримує додаток
