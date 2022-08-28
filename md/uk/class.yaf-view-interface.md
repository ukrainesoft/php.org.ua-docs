Клас YafViewInterface

-   [« Yaf\_Action\_Abstract::getControllerName](yaf-controller-abstract.getcontrollername.html)
    
-   [Yaf\_View\_Interface::assign »](yaf-view-interface.assign.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafViewInterface
    

# Клас YafViewInterface

(Yaf >=1.0.0)

## Вступ

Yaf надає розробникам можливість використовувати їх власний движок відображення, що відрізняється від вбудованого [Yaf\_View\_Simple](class.yaf-view-simple.html). Приклад реалізації дивіться у описі [Yaf\_Dispatcher::setView()](yaf-dispatcher.setview.html)

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_View_Interface
     
     {
    

    /* Методы */
    
   abstract public assign(string $name, string $value = ?): bool
abstract public display(string $tpl, array $tpl_vars = ?): bool
abstract public getScriptPath(): void
abstract public render(string $tpl, array $tpl_vars = ?): string
abstract public setScriptPath(string $template_dir): void

   }
```

## Зміст

-   [Yaf\_View\_Interface::assign](yaf-view-interface.assign.html) — Призначає значення для движка відображення
-   [Yaf\_View\_Interface::display](yaf-view-interface.display.html) — Малює та виводить шаблон
-   [Yaf\_View\_Interface::getScriptPath](yaf-view-interface.getscriptpath.html) - Призначення getScriptPath
-   [Yaf\_View\_Interface::render](yaf-view-interface.render.html) — Малює шаблон
-   [Yaf\_View\_Interface::setScriptPath](yaf-view-interface.setscriptpath.html) - Призначення setScriptPath