---
navigation:
  - wincache.setup.md: « Встановлення та налаштування
  - wincache.installation.md: Установка »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Вимоги
---
## Вимоги

В даний момент модуль підтримується лише для наступних конфігурацій:

Windows OS:

-   Windows XP SP3 з IIS 5.1 та [» FastCGI Extension](http://www.iis.net/extensions/fastcgi)
-   Windows Server 2003 з IIS 6.0 та [» FastCGI Extension](http://www.iis.net/extensions/fastcgi)
-   Windows Vista SP1 з IIS 7.0 та FastCGI Module
-   Windows Server 2008 з IIS 7.0 та FastCGI Module
-   Windows 7 з IIS 7.5 та FastCGI Module
-   Windows Server 2008 R2 з IIS 7.5 та FastCGI Module

PHP:

-   PHP 5.2.X, не потокобезпечне складання
-   PHP 5.3 X86, не потокобезпечне VC9 складання

> **Зауваження**: Модуль WinCache може використовуватися тільки якщо IIS налаштований використовувати PHP через FastCGI.
