---
navigation:
  - wincache.win32build.building.md: « Компіляція та складання
  - book.xhprof.md: Xhprof »
  - index.md: PHP Manual
  - wincache.win32build.md: Сборка для Windows
title: Перевірка збирання
---
## Перевірка збирання

Наступні кроки описують процес перевірки того, що модуль був зібраний коректно:

1.  Перейдіть до папки, де знаходиться скомпільований PHP
    
2.  Виконайте команду:
    
    php.exe -n -d extension=phpwincache.dll -re wincache
    
    Якщо модуль зібраний правильно, у виведенні цієї команди будуть показані INI-директиви та функції, що підтримуються WinCache.
