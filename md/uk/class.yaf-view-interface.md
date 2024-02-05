---
navigation:
  - yaf-controller-abstract.getcontrollername.md: '« Yaf\_Action\_Abstract::getControllerName'
  - yaf-view-interface.assign.md: 'Yaf\_View\_Interface::assign »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_View\_Interface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_View\_Interface

(Yaf >=1.0.0)

## Вступ

Yaf надає розробникам можливість використовувати їх власний движок відображення, що відрізняється від вбудованого [Yaf\_View\_Simple](class.yaf-view-simple.md)Пример реализации смотрите в описании[Yaf\_Dispatcher::setView()](yaf-dispatcher.setview.md)

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

-   [Yaf\_View\_Interface::assign](yaf-view-interface.assign.md)— Призначає значення для движка відображення
-   [Yaf\_View\_Interface::display](yaf-view-interface.display.md)— Малює та виводить шаблон
-   [Yaf\_View\_Interface::getScriptPath](yaf-view-interface.getscriptpath.md) \- Призначення getScriptPath
-   [Yaf\_View\_Interface::render](yaf-view-interface.render.md)— Малює шаблон
-   [Yaf\_View\_Interface::setScriptPath](yaf-view-interface.setscriptpath.md) \- Призначення setScriptPath
