---
navigation:
  - yaf-view-interface.setscriptpath.md: '« YafViewInterface::setScriptPath'
  - yaf-view-simple.assign.md: 'YafViewSimple::assign »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafViewSimple
---
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

-   [YafViewSimple::assign](yaf-view-simple.assign.md) - Призначити значення
-   [YafViewSimple::assignRef](yaf-view-simple.assignref.md) — Призначення assignRef
-   [YafViewSimple::clear](yaf-view-simple.clear.md) - Скидає призначені значення
-   [YafViewSimple::construct](yaf-view-simple.construct.md) - Конструктор класу YafViewSimple
-   [YafViewSimple::display](yaf-view-simple.display.md) — Малює та відображає
-   [YafViewSimple::eval](yaf-view-simple.eval.md) — Малює шаблон
-   [YafViewSimple::get](yaf-view-simple.get.md) — Отримує призначену змінну
-   [YafViewSimple::getScriptPath](yaf-view-simple.getscriptpath.md) — Отримує каталог шаблонів
-   [YafViewSimple::isset](yaf-view-simple.isset.md) - Призначення isset
-   [YafViewSimple::render](yaf-view-simple.render.md) — Малює шаблон
-   [YafViewSimple::set](yaf-view-simple.set.md) - Встановлює значення для двигуна
-   [YafViewSimple::setScriptPath](yaf-view-simple.setscriptpath.md) — Встановлює каталог шаблонів
