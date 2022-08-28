Призначення setScriptPath

-   [« Yaf\_View\_Interface::render](yaf-view-interface.render.html)
    
-   [Yaf\_View\_Simple »](class.yaf-view-simple.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_View\_Interface](class.yaf-view-interface.html)
    
-   Призначення setScriptPath
    

# YafViewInterface::setScriptPath

(Yaf >=1.0.0)

YafViewInterface::setScriptPath — Призначення setScriptPath

### Опис

```methodsynopsis
abstract public Yaf_View_Interface::setScriptPath(string $template_dir): void
```

Встановлює базовий каталог шаблонів, зазвичай викликається в [Yaf\_Dispatcher](class.yaf-dispatcher.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`template_dir`

Абсолютний шлях до каталогу шаблонів за промовчанням [Yaf\_Dispatcher](class.yaf-dispatcher.html) використовується [application.directory](yaf.appconfig.html#configuration.yaf.directory) . "/views".

### Значення, що повертаються