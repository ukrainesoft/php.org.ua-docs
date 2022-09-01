---
navigation:
  - yaf-view-interface.render.html: '« YafViewInterface::render'
  - class.yaf-view-simple.html: YafViewSimple »
  - index.md: PHP Manual
  - class.yaf-view-interface.html: YafViewInterface
title: 'YafViewInterface::setScriptPath'
---
# YafViewInterface::setScriptPath

(Yaf >=1.0.0)

YafViewInterface::setScriptPath — Призначення setScriptPath

### Опис

```methodsynopsis
abstract public Yaf_View_Interface::setScriptPath(string $template_dir): void
```

Встановлює базовий каталог шаблонів, зазвичай викликається в [YafDispatcher](class.yaf-dispatcher.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`template_dir`

Абсолютний шлях до каталогу шаблонів за промовчанням [YafDispatcher](class.yaf-dispatcher.html) використовується [application.directory](yaf.appconfig.html#configuration.yaf.directory) . "/views".

### Значення, що повертаються
