---
navigation:
  - class.yaf-plugin-abstract.md: « Yaf\_Plugin\_Abstract
  - yaf-plugin-abstract.dispatchloopstartup.md: 'Yaf\_Plugin\_Abstract::dispatchLoopStartup »'
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.md: Yaf\_Plugin\_Abstract
title: 'Yaf\_Plugin\_Abstract::dispatchLoopShutdown'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Plugin\_Abstract::dispatchLoopShutdown

(Yaf >=1.0.0)

Yaf\_Plugin\_Abstract::dispatchLoopShutdown — Призначення dispatchLoopShutdown

### Опис

```methodsynopsis
public Yaf_Plugin_Abstract::dispatchLoopShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
```

Це останній перехоплювач у системі підключень плагінів Yaf, якщо плагін реалізує цей метод, то він буде викликаний після завершення циклу диспетчеризації.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`request`

`response`

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Plugin\_Abstract::routerStartup()](yaf-plugin-abstract.routerstartup.md) \- Перехоплювач RouterStartup
-   [Yaf\_Plugin\_Abstract::routerShutdown()](yaf-plugin-abstract.routershutdown.md) \- Призначення routerShutdown
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) \- Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::preDispatch()](yaf-plugin-abstract.predispatch.md) \- Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) \- Призначення postDispatch
