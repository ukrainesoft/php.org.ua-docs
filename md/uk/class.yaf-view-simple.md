Клас YafViewSimple

-   [« YafViewInterface::setScriptPath](yaf-view-interface.setscriptpath.html)
    
-   [YafViewSimple::assign »](yaf-view-simple.assign.html)
    
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

-   [YafViewSimple::assign](yaf-view-simple.assign.html) - Призначити значення
-   [YafViewSimple::assignRef](yaf-view-simple.assignref.html) — Призначення assignRef
-   [YafViewSimple::clear](yaf-view-simple.clear.html) - Скидає призначені значення
-   [YafViewSimple::construct](yaf-view-simple.construct.html) - Конструктор класу YafViewSimple
-   [YafViewSimple::display](yaf-view-simple.display.html) — Малює та відображає
-   [YafViewSimple::eval](yaf-view-simple.eval.html) — Малює шаблон
-   [YafViewSimple::get](yaf-view-simple.get.html) — Отримує призначену змінну
-   [YafViewSimple::getScriptPath](yaf-view-simple.getscriptpath.html) — Отримує каталог шаблонів
-   [YafViewSimple::isset](yaf-view-simple.isset.html) - Призначення isset
-   [YafViewSimple::render](yaf-view-simple.render.html) — Малює шаблон
-   [YafViewSimple::set](yaf-view-simple.set.html) - Встановлює значення для двигуна
-   [YafViewSimple::setScriptPath](yaf-view-simple.setscriptpath.html) — Встановлює каталог шаблонів