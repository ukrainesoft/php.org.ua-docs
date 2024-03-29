---
navigation:
  - ui-size.setwidth.md: '« UI\\Size::setWidth'
  - ui-window.add.md: 'UI\\Window::add »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Вікно
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Window::add](ui-window.add.md)— Додати елемент керування
-   [UI\\Window::\_\_construct](ui-window.construct.md) \- Створити новий об'єкт Window
-   [UI\\Window::error](ui-window.error.md) \- Показати блок помилки
-   [UI\\Window::getSize](ui-window.getsize.md)— Отримати розмір вікна
-   [UI\\Window::getTitle](ui-window.gettitle.md) \- Отримати заголовок
-   [UI\\Window::hasBorders](ui-window.hasborders.md) \- Визначення рамки
-   [UI\\Window::hasMargin](ui-window.hasmargin.md) \- Визначення полів
-   [UI\\Window::isFullScreen](ui-window.isfullscreen.md)— Визначення повного екрану
-   [UI\\Window::msg](ui-window.msg.md)— Показати блок повідомлення
-   [UI\\Window::onClosing](ui-window.onclosing.md) \- Callback-функція закриття
-   [UI\\Window::open](ui-window.open.md)— Відкрити діалогове вікно
-   [UI\\Window::save](ui-window.save.md)— Зберегти діалогове вікно
-   [UI\\Window::setBorders](ui-window.setborders.md)— Використання рамок
-   [UI\\Window::setFullScreen](ui-window.setfullscreen.md)— Використання повного екрану
-   [UI\\Window::setMargin](ui-window.setmargin.md)— Використання поля
-   [UI\\Window::setSize](ui-window.setsize.md) \- Встановити розмір
-   [UI\\Window::setTitle](ui-window.settitle.md) \- Заголовок вікна
