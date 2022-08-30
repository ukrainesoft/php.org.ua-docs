Елемент управління "Таб"

-   [« UIExecutor::setInterval](ui-executor.setinterval.html)
    
-   [ОЙControlsTab::append »](ui-controls-tab.append.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙ](book.ui.md)
    
-   Елемент управління "Таб"
    

# Елемент управління "Таб"

(UI 0.9.9)

## Вступ

Таб може містити багато вибраних користувачем сторінок елементів управління, кожна з якої має заголовок.

## Огляд класів

```classsynopsis



    
     
      class UI\Controls\Tab
     

     
      extends
       UI\Control
     
     {


    /* Свойства */
    
     protected
      $controls;


    /* Методы */
    
   public append(string $name, UI\Control $control): int
public delete(int $index): bool
public hasMargin(int $page): bool
public insertAt(string $name, int $page, UI\Control $control)
public pages(): int
public setMargin(int $page, bool $margin)


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

Містить елементи керування, не варто змінювати напряму

## Зміст

-   [ОЙControlsTab::append](ui-controls-tab.append.html) - Додати сторінку
-   [ОЙControlsTab::delete](ui-controls-tab.delete.html) — Видалити сторінку
-   [ОЙControlsTab::hasMargin](ui-controls-tab.hasmargin.html) - Визначення поля
-   [ОЙControlsTab::insertAt](ui-controls-tab.insertat.html) - Вставити сторінку
-   [ОЙControlsTab::pages](ui-controls-tab.pages.html) - Кількість сторінок
-   [ОЙControlsTab::setMargin](ui-controls-tab.setmargin.html) - Встановити поле