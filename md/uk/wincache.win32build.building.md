---
navigation:
  - wincache.win32build.prereq.md: « Пререквізити
  - wincache.win32build.verify.md: Перевірка збирання »
  - index.md: PHP Manual
  - wincache.win32build.md: Складання для Windows
title: Компіляція та складання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Компіляція та складання

Наступні кроки описують, як компілювати та збирати WinCache під Windows OS:

1.  Відкрийте консоль командного рядка
    
2.  Перейдіть до папки з вихідними кодами PHP
    
3.  Виконайте команду:
    
    cscript.exe win32\\build\\buildconf.js
    
4.  Виконайте команду:
    
    configure.bat --help
    
    Висновок міститиме новий прапор`--enable-wincache`
    
5.  Виконайте команду:
    
    configure.js\[всі опції для збирання PHP\]--enable-wincache
    
    `--enable-wincache`це єдина додаткова опція, яка потрібна для правильного складання модуля WinCache. Ця опція збере WinCache і статично пов'язуватиме його з PHP dll. Щоб створити модуль WinCache як автономну бібліотеку DLL, використовуйте параметр`--enable-wincache=shared`
    
6.  Виконайте команду:
    
    nmake
