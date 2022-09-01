---
navigation:
  - ui-size.setwidth.html: '« UISize::setWidth'
  - ui-window.add.html: 'ОЙWindow::add »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Вікно
---
# Вікно

(UI 0.9.9)

## Вступ

Представляє інтерфейс вікна

## Огляд класів

```classsynopsis



    
     
      class UI\Window
     

     
      extends
       UI\Control
     
     {

    /* Свойства */
    
     protected
      $controls;


    /* Конструктор */
    
   public __construct(string $title, Size $size, bool $menu = false)


    /* Методы */
    public add(UI\Control $control)
public error(string $title, string $msg)
public getSize(): UI\Size
public getTitle(): string
public hasBorders(): bool
public hasMargin(): bool
public isFullScreen(): bool
public msg(string $title, string $msg)
protected onClosing(): int
public open(): string
public save(): string
public setBorders(bool $borders)
public setFullScreen(bool $full)
public setMargin(bool $margin)
public setSize(UI\Size $size)
public setTitle(string $title)


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

## Властивості

controls

Містить елементи керування, не слід використовувати безпосередньо

## Зміст

-   [ОЙWindow::add](ui-window.add.md) — Додати елемент керування
-   [ОЙWindow::construct](ui-window.construct.md) - Створити новий об'єкт Window
-   [ОЙWindow::error](ui-window.error.md) - Показати блок помилки
-   [ОЙWindow::getSize](ui-window.getsize.md) — Отримати розмір вікна
-   [ОЙWindow::getTitle](ui-window.gettitle.md) - Отримати заголовок
-   [ОЙWindow::hasBorders](ui-window.hasborders.md) - Визначення рамки
-   [ОЙWindow::hasMargin](ui-window.hasmargin.md) - Визначення полів
-   [ОЙWindow::isFullScreen](ui-window.isfullscreen.md) — Визначення повного екрану
-   [ОЙWindow::msg](ui-window.msg.md) — Показати блок повідомлення
-   [ОЙWindow::onClosing](ui-window.onclosing.md) - Callback-функція закриття
-   [ОЙWindow::open](ui-window.open.md) — Відкрити діалогове вікно
-   [ОЙWindow::save](ui-window.save.md) — Зберегти діалогове вікно
-   [ОЙWindow::setBorders](ui-window.setborders.md) — Використання рамок
-   [ОЙWindow::setFullScreen](ui-window.setfullscreen.md) — Використання повного екрану
-   [ОЙWindow::setMargin](ui-window.setmargin.md) — Використання поля
-   [ОЙWindow::setSize](ui-window.setsize.md) - Встановити розмір
-   [ОЙWindow::setTitle](ui-window.settitle.md) - Заголовок вікна
