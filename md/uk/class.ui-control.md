---
navigation:
  - ui-window.settitle.html: '« UIWindow::setTitle'
  - ui-control.destroy.html: 'ОЙControl::destroy »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Елемент управління
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

-   [ОЙControl::destroy](ui-control.destroy.md) — Знищити керуючий елемент
-   [ОЙControl::disable](ui-control.disable.md) — Вимкнути керуючий елемент
-   [ОЙControl::enable](ui-control.enable.md) — Включити елемент керування
-   [ОЙControl::getParent](ui-control.getparent.md) — Отримати батьківський керуючий елемент
-   [ОЙControl::getTopLevel](ui-control.gettoplevel.md) — Здобути верхній рівень
-   [ОЙControl::hide](ui-control.hide.md) — Приховати елемент керування
-   [ОЙControl::isEnabled](ui-control.isenabled.md) — Визначити, чи включений елемент керування
-   [ОЙControl::isVisible](ui-control.isvisible.md) — Визначити, чи видимий елемент керування
-   [ОЙControl::setParent](ui-control.setparent.md) — Встановити батьківський елемент управління
-   [ОЙControl::show](ui-control.show.md) - Показати керуючий елемент
