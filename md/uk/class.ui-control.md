---
navigation:
  - ui-window.settitle.md: '« UI\\Window::setTitle'
  - ui-control.destroy.md: 'UI\\Control::destroy »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Елемент управління
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Елемент управління

(UI 0.9.9)

## Вступ

Це закритий базовий клас для всіх елементів керування інтерфейсу користувача.

## Огляд класів

```classsynopsis



    
     
      final
      class UI\Control
     
     {


    /* Методы */
    
   public destroy()
public disable()
public enable()
public getParent(): UI\Control
public getTopLevel(): int
public hide()
public isEnabled(): bool
public isVisible(): bool
public setParent(UI\Control $parent)
public show()

   }
```

## Зміст

-   [UI\\Control::destroy](ui-control.destroy.md)— Знищити керуючий елемент
-   [UI\\Control::disable](ui-control.disable.md)— Вимкнути керуючий елемент
-   [UI\\Control::enable](ui-control.enable.md)— Включити елемент керування
-   [UI\\Control::getParent](ui-control.getparent.md)— Отримати батьківський керуючий елемент
-   [UI\\Control::getTopLevel](ui-control.gettoplevel.md)— Здобути верхній рівень
-   [UI\\Control::hide](ui-control.hide.md)— Приховати елемент керування
-   [UI\\Control::isEnabled](ui-control.isenabled.md)— Визначити, чи включений елемент керування
-   [UI\\Control::isVisible](ui-control.isvisible.md)— Визначити, чи видимий елемент керування
-   [UI\\Control::setParent](ui-control.setparent.md)— Встановити батьківський елемент управління
-   [UI\\Control::show](ui-control.show.md) \- Показати керуючий елемент
