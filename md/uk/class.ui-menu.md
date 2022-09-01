---
navigation:
  - ui-control.show.html: '« UIControl::show'
  - ui-menu.append.html: 'ОЙMenu::append »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Меню
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

-   [ОЙMenu::append](ui-menu.append.md) - Додати пункт меню
-   [ОЙMenu::appendAbout](ui-menu.appendabout.md) — Додати пункт меню About
-   [ОЙMenu::appendCheck](ui-menu.appendcheck.md) - Додати пункт меню з чекбоксом
-   [ОЙMenu::appendPreferences](ui-menu.appendpreferences.md) - Додати пункт меню "Налаштування" (Preferences)
-   [ОЙMenu::appendQuit](ui-menu.appendquit.md) - Додати пункт меню "Вихід" (Quit)
-   [ОЙMenu::appendSeparator](ui-menu.appendseparator.md) - Додати пункт меню "Розділювач" (Separator)
-   [ОЙMenu::construct](ui-menu.construct.md) — Створити новий об'єкт
