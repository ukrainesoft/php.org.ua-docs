---
navigation:
  - yaf-plugin-abstract.routershutdown.md: '« Yaf\_Plugin\_Abstract::routerShutdown'
  - class.yaf-registry.md: Yaf\_Registry »
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.md: Yaf\_Plugin\_Abstract
title: 'Yaf\_Plugin\_Abstract::routerStartup'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Plugin\_Abstract::routerStartup

(Yaf >=1.0.0)

Yaf\_Plugin\_Abstract::routerStartup — Перехоплювач RouterStartup

### Опис

```methodsynopsis
public Yaf_Plugin_Abstract::routerStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
```

Це найраніший перехоплювач у системі плагінів Yaf, якщо плагін реалізує цей метод, то він буде викликаний перед маршрутизацією запиту.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`request`

`response`

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Plugin\_Abstract::routerShutdown()](yaf-plugin-abstract.routershutdown.md) \- Призначення routerShutdown
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) \- Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::preDispatch()](yaf-plugin-abstract.predispatch.md) \- Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) \- Призначення postDispatch
-   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.md) \- Призначення dispatchLoopShutdown
