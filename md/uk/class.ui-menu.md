---
navigation:
  - ui-control.show.md: '« UI\\Control::show'
  - ui-menu.append.md: 'UI\\Menu::append »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Меню
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [UI\\Menu::append](ui-menu.append.md) \- Додати пункт меню
-   [UI\\Menu::appendAbout](ui-menu.appendabout.md)— Додати пункт меню About
-   [UI\\Menu::appendCheck](ui-menu.appendcheck.md) \- Додати пункт меню з чекбоксом
-   [UI\\Menu::appendPreferences](ui-menu.appendpreferences.md) - Додати пункт меню "Налаштування" (Preferences)
-   [UI\\Menu::appendQuit](ui-menu.appendquit.md) - Додати пункт меню "Вихід" (Quit)
-   [UI\\Menu::appendSeparator](ui-menu.appendseparator.md) - Додати пункт меню "Розділювач" (Separator)
-   [UI\\Menu::\_\_construct](ui-menu.construct.md)— Створити новий об'єкт
