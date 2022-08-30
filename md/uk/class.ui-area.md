Area

-   [« UIMenuItem::setChecked](ui-menuitem.setchecked.html)
    
-   [ОЙArea::onDraw »](ui-area.ondraw.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Area
    

# Area

(UI 0.9.9)

## Вступ

Область (Area) являє собою полотно, яке можна використовувати для малювання та реагування на події миші та клавіш.

## Огляд класів

```classsynopsis



    
     
      class UI\Area
     

     
      extends
       UI\Control
     
     {

    /* Константы */
    
     const
     int
      Ctrl;

    const
     int
      Alt;

    const
     int
      Shift;

    const
     int
      Super;

    const
     int
      Down;

    const
     int
      Up;


    /* Методы */
    
   protected onDraw(    UI\Draw\Pen $pen,    UI\Size $areaSize,    UI\Point $clipPoint,    UI\Size $clipSize)
protected onKey(string $key, int $ext, int $flags)
protected onMouse(UI\Point $areaPoint, UI\Size $areaSize, int $flags)
public redraw()
public scrollTo(UI\Point $point, UI\Size $size)
public setSize(UI\Size $size)


    /* Наследуемые методы */
    public UI\Control::destroy()
public UI\Control::disable()
public UI\Control::enable()
public UI\Control::getParent(): UI\Control
public UI\Control::getTopLevel(): int
public UI\Control::hide()
public UI\Control::isEnabled(): bool
public UI\Control::isVisible(): bool
public UI\Control::setParent(UI\Control $parent)
public UI\Control::show()


   }
```

## Обумовлені константи

**`UI\Area::Ctrl`**

Має бути встановлений у модифікаторах, переданих подіям клавіш і миші, коли активна клавіша CTRL

**`UI\Area::Alt`**

Повинен бути встановлений у модифікаторах, переданих подіям клавіш та миші, коли активна клавіша ALT

**`UI\Area::Shift`**

Повинен бути встановлений у модифікаторах, переданих подіям клавіш та миші, коли активна клавіша SHIFT

**`UI\Area::Super`**

**`UI\Area::Down`**

Має бути встановлений у модифікаторах, переданих подіям клавіатури та миші

**`UI\Area::Up`**

Має бути встановлений у модифікаторах, переданих подіям клавіатури та миші

## Зміст

-   [ОЙArea::onDraw](ui-area.ondraw.html) — Функція зворотного виклику під час малювання
-   [ОЙArea::onKey](ui-area.onkey.html) — Функція зворотного дзвінка під час натискання
-   [ОЙArea::onMouse](ui-area.onmouse.html) — Функція зворотного дзвінка миші
-   [ОЙArea::redraw](ui-area.redraw.html) - Перемалювати область
-   [ОЙArea::scrollTo](ui-area.scrollto.html) - Прокрутити область
-   [ОЙArea::setSize](ui-area.setsize.html) - Встановити розмір