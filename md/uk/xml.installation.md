---
navigation:
  - xml.requirements.md: « Вимоги
  - xml.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - xml.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Модуль увімкнено за замовчуванням. Він може бути вимкнений під час виконання опцією: **\--disable-xml**

Ці функції включені за умовчанням під час використання стандартної бібліотеки expat. Ви можете вимкнути підтримку XML за допомогою **\--disable-xml**. Якщо ви зібрали PHP як модуль для Apache 1.3.9 або пізнішої версії, PHP автоматично використовуватиме стандартну бібліотеку expat з Apache. Якщо ви не хочете використовувати стандартну бібліотеку expat, то вам необхідно налаштувати PHP опцію **\--with-expat-dir=DIR**, де DIR - шлях до настановної директорії бібліотеки expat.

Версія PHP для Windows має вбудовану підтримку цього модуля. Тобто для виклику цих функцій не потрібно завантаження додаткових модулів.
