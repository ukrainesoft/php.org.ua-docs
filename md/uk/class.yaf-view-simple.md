---
navigation:
  - yaf-view-interface.setscriptpath.md: '« Yaf\_View\_Interface::setScriptPath'
  - yaf-view-simple.assign.md: 'Yaf\_View\_Simple::assign »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_View\_Simple
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_View\_Simple

(Yaf >=1.0.0)

## Вступ

**Yaf\_View\_Simple** - Це вбудований шаблонний двигун Yaf. Він простий, але швидкий та підтримує лише шаблони PHP-скриптів.

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

\_tpl\_vars

\_tpl\_dir

## Зміст

-   [Yaf\_View\_Simple::assign](yaf-view-simple.assign.md) \- Призначити значення
-   [Yaf\_View\_Simple::assignRef](yaf-view-simple.assignref.md)— Призначення assignRef
-   [Yaf\_View\_Simple::clear](yaf-view-simple.clear.md) \- Скидає призначені значення
-   [Yaf\_View\_Simple::\_\_construct](yaf-view-simple.construct.md) \- Конструктор класу Yaf\_View\_Simple
-   [Yaf\_View\_Simple::display](yaf-view-simple.display.md)— Малює та відображає
-   [Yaf\_View\_Simple::eval](yaf-view-simple.eval.md)— Малює шаблон
-   [Yaf\_View\_Simple::\_\_get](yaf-view-simple.get.md)— Отримує призначену змінну
-   [Yaf\_View\_Simple::getScriptPath](yaf-view-simple.getscriptpath.md)— Отримує каталог шаблонів
-   [Yaf\_View\_Simple::\_\_isset](yaf-view-simple.isset.md) \- Призначення\_\_isset
-   [Yaf\_View\_Simple::render](yaf-view-simple.render.md)— Малює шаблон
-   [Yaf\_View\_Simple::\_\_set](yaf-view-simple.set.md) \- Встановлює значення для двигуна
-   [Yaf\_View\_Simple::setScriptPath](yaf-view-simple.setscriptpath.md)— Встановлює каталог шаблонів
