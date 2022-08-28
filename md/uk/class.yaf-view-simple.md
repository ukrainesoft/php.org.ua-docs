Клас YafViewSimple

-   [« Yaf\_View\_Interface::setScriptPath](yaf-view-interface.setscriptpath.html)
    
-   [Yaf\_View\_Simple::assign »](yaf-view-simple.assign.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafViewSimple
    

# Клас YafViewSimple

(Yaf >=1.0.0)

## Вступ

**YafViewSimple** - Це вбудований шаблонний двигун Yaf. Він простий, але швидкий та підтримує лише шаблони PHP-скриптів.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_View_Simple
     

     implements 
       Yaf_View_Interface {
    
    /* Свойства */
    
     protected
      $_tpl_vars;

    protected
      $_tpl_dir;



    /* Методы */
    
   final public __construct(string $template_dir, array $options = ?)

    public assign(string $name, mixed $value = ?): bool
public assignRef(string $name, mixed &$value): bool
public clear(string $name = ?): bool
public display(string $tpl, array $tpl_vars = ?): bool
public eval(string $tpl_content, array $tpl_vars = ?): string
public __get(string $name = ?): void
public getScriptPath(): string
public __isset(string $name): void
public render(string $tpl, array $tpl_vars = ?): string
public __set(string $name, mixed $value): void
public setScriptPath(string $template_dir): bool

   }
```

## Властивості

tplvars

tpldir

## Зміст

-   [Yaf\_View\_Simple::assign](yaf-view-simple.assign.html) - Призначити значення
-   [Yaf\_View\_Simple::assignRef](yaf-view-simple.assignref.html) — Призначення assignRef
-   [Yaf\_View\_Simple::clear](yaf-view-simple.clear.html) - Скидає призначені значення
-   [Yaf\_View\_Simple::\_\_construct](yaf-view-simple.construct.html) - Конструктор класу YafViewSimple
-   [Yaf\_View\_Simple::display](yaf-view-simple.display.html) — Малює та відображає
-   [Yaf\_View\_Simple::eval](yaf-view-simple.eval.html) — Малює шаблон
-   [Yaf\_View\_Simple::\_\_get](yaf-view-simple.get.html) — Отримує призначену змінну
-   [Yaf\_View\_Simple::getScriptPath](yaf-view-simple.getscriptpath.html) — Отримує каталог шаблонів
-   [Yaf\_View\_Simple::\_\_isset](yaf-view-simple.isset.html) - Призначення isset
-   [Yaf\_View\_Simple::render](yaf-view-simple.render.html) — Малює шаблон
-   [Yaf\_View\_Simple::\_\_set](yaf-view-simple.set.html) - Встановлює значення для двигуна
-   [Yaf\_View\_Simple::setScriptPath](yaf-view-simple.setscriptpath.html) — Встановлює каталог шаблонів