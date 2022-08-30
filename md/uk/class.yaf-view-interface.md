Клас YafViewInterface

-   [« YafActionAbstract::getControllerName](yaf-controller-abstract.getcontrollername.html)
    
-   [YafViewInterface::assign »](yaf-view-interface.assign.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafViewInterface
    

# Клас YafViewInterface

(Yaf >=1.0.0)

## Вступ

Yaf надає розробникам можливість використовувати їх власний движок відображення, що відрізняється від вбудованого [YafViewSimple](class.yaf-view-simple.html). Приклад реалізації дивіться у описі [YafDispatcher::setView()](yaf-dispatcher.setview.html)

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

-   [YafViewInterface::assign](yaf-view-interface.assign.html) — Призначає значення для движка відображення
-   [YafViewInterface::display](yaf-view-interface.display.html) — Малює та виводить шаблон
-   [YafViewInterface::getScriptPath](yaf-view-interface.getscriptpath.html) - Призначення getScriptPath
-   [YafViewInterface::render](yaf-view-interface.render.html) — Малює шаблон
-   [YafViewInterface::setScriptPath](yaf-view-interface.setscriptpath.html) - Призначення setScriptPath