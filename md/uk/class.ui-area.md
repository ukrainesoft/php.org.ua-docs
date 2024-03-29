---
navigation:
  - ui-menuitem.setchecked.md: '« UI\\MenuItem::setChecked'
  - ui-area.ondraw.md: 'UI\\Area::onDraw »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Area
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Area::onDraw](ui-area.ondraw.md)— Функція зворотного виклику під час малювання
-   [UI\\Area::onKey](ui-area.onkey.md)— Функція зворотного дзвінка під час натискання
-   [UI\\Area::onMouse](ui-area.onmouse.md)— Функція зворотного дзвінка миші
-   [UI\\Area::redraw](ui-area.redraw.md)— Перемалювати область
-   [UI\\Area::scrollTo](ui-area.scrollto.md) \- Прокрутити область
-   [UI\\Area::setSize](ui-area.setsize.md) \- Встановити розмір
