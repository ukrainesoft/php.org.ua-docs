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

-   [ОЙWindow::add](ui-window.add.html) — Додати елемент керування
-   [ОЙWindow::construct](ui-window.construct.html) - Створити новий об'єкт Window
-   [ОЙWindow::error](ui-window.error.html) - Показати блок помилки
-   [ОЙWindow::getSize](ui-window.getsize.html) — Отримати розмір вікна
-   [ОЙWindow::getTitle](ui-window.gettitle.html) - Отримати заголовок
-   [ОЙWindow::hasBorders](ui-window.hasborders.html) - Визначення рамки
-   [ОЙWindow::hasMargin](ui-window.hasmargin.html) - Визначення полів
-   [ОЙWindow::isFullScreen](ui-window.isfullscreen.html) — Визначення повного екрану
-   [ОЙWindow::msg](ui-window.msg.html) — Показати блок повідомлення
-   [ОЙWindow::onClosing](ui-window.onclosing.html) - Callback-функція закриття
-   [ОЙWindow::open](ui-window.open.html) — Відкрити діалогове вікно
-   [ОЙWindow::save](ui-window.save.html) — Зберегти діалогове вікно
-   [ОЙWindow::setBorders](ui-window.setborders.html) — Використання рамок
-   [ОЙWindow::setFullScreen](ui-window.setfullscreen.html) — Використання повного екрану
-   [ОЙWindow::setMargin](ui-window.setmargin.html) — Використання поля
-   [ОЙWindow::setSize](ui-window.setsize.html) - Встановити розмір
-   [ОЙWindow::setTitle](ui-window.settitle.html) - Заголовок вікна
