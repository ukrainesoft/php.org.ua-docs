Меню

-   [« UIControl::show](ui-control.show.html)
    
-   [ОЙMenu::append »](ui-menu.append.html)
    
-   [PHP Manual](index.md)
    
-   [ОЙ](book.ui.md)
    
-   Меню
    

# Меню

(UI 0.9.9)

## Вступ

Меню має бути створене до першого вікна і може відображатись у будь-якому вікні

## Огляд класів

```classsynopsis



    
     
      class UI\Menu
     
     {


     /* Конструктор */
    
   public __construct(string $name)


    /* Методы */
    public append(string $name, string $type = UI\MenuItem::class): UI\MenuItem
public appendAbout(string $type = UI\MenuItem::class): UI\MenuItem
public appendCheck(string $name, string $type = UI\MenuItem::class): UI\MenuItem
public appendPreferences(string $type = UI\MenuItem::class): UI\MenuItem
public appendQuit(string $type = UI\MenuItem::class): UI\MenuItem
public appendSeparator()

   }
```

## Зміст

-   [ОЙMenu::append](ui-menu.append.html) - Додати пункт меню
-   [ОЙMenu::appendAbout](ui-menu.appendabout.html) — Додати пункт меню About
-   [ОЙMenu::appendCheck](ui-menu.appendcheck.html) - Додати пункт меню з чекбоксом
-   [ОЙMenu::appendPreferences](ui-menu.appendpreferences.html) - Додати пункт меню "Налаштування" (Preferences)
-   [ОЙMenu::appendQuit](ui-menu.appendquit.html) - Додати пункт меню "Вихід" (Quit)
-   [ОЙMenu::appendSeparator](ui-menu.appendseparator.html) - Додати пункт меню "Розділювач" (Separator)
-   [ОЙMenu::construct](ui-menu.construct.html) — Створити новий об'єкт