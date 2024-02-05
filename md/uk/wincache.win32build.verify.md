---
navigation:
  - wincache.win32build.building.md: « Компіляція та складання
  - book.xhprof.md: Xhprof »
  - index.md: PHP Manual
  - wincache.win32build.md: Складання для Windows
title: Перевірка збирання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Перевірка збирання

Наступні кроки описують процес перевірки того, що модуль був зібраний коректно:

1.  Перейдіть до папки, де знаходиться скомпільований PHP
    
2.  Виконайте команду:
    
    php.exe -n -d extension=php\_wincache.dll -re wincache
    
    Якщо модуль зібраний правильно, у виведенні цієї команди будуть показані INI-директиви та функції, що підтримуються WinCache.
