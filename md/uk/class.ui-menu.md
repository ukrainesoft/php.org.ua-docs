Меню

-   [« UI\\Control::show](ui-control.show.html)
    
-   [UI\\Menu::append »](ui-menu.append.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
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

-   [UI\\Menu::append](ui-menu.append.html) - Додати пункт меню
-   [UI\\Menu::appendAbout](ui-menu.appendabout.html) — Додати пункт меню About
-   [UI\\Menu::appendCheck](ui-menu.appendcheck.html) - Додати пункт меню з чекбоксом
-   [UI\\Menu::appendPreferences](ui-menu.appendpreferences.html) - Додати пункт меню "Налаштування" (Preferences)
-   [UI\\Menu::appendQuit](ui-menu.appendquit.html) - Додати пункт меню "Вихід" (Quit)
-   [UI\\Menu::appendSeparator](ui-menu.appendseparator.html) - Додати пункт меню "Розділювач" (Separator)
-   [UI\\Menu::\_\_construct](ui-menu.construct.html) — Створити новий об'єкт