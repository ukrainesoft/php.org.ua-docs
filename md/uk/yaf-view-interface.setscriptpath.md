---
navigation:
  - yaf-view-interface.render.md: '« YafViewInterface::render'
  - class.yaf-view-simple.md: YafViewSimple »
  - index.md: PHP Manual
  - class.yaf-view-interface.md: YafViewInterface
title: 'YafViewInterface::setScriptPath'
---
# YafViewInterface::setScriptPath

(Yaf >=1.0.0)

YafViewInterface::setScriptPath — Призначення setScriptPath

### Опис

```methodsynopsis
abstract public Yaf_View_Interface::setScriptPath(string $template_dir): void
```

Встановлює базовий каталог шаблонів, зазвичай викликається в [YafDispatcher](class.yaf-dispatcher.md)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`template_dir`

Абсолютний шлях до каталогу шаблонів за промовчанням [YafDispatcher](class.yaf-dispatcher.md) використовується [application.directory](yaf.appconfig.md#configuration.yaf.directory) . "/views".

### Значення, що повертаються
