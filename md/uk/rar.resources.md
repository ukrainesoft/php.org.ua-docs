---
navigation:
  - rar.configuration.md: « Налаштування під час виконання
  - rar.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - rar.setup.md: Встановлення та налаштування
title: Типи ресурсів
---
## Типи ресурсів

Цей модуль використовує три внутрішні ресурси: дескриптор файлу, що повертається функцією [raropen()](rararchive.open.md) [RarArchive](class.rararchive.md), вміст архіву, що повертається функціями [rarlist()](rararchive.getentries.md) і [rarentryget()](rararchive.getentry.md) [RarEntry](class.rarentry.md) та тип винятків [RarException](class.rarexception.md)

Цей модуль також реєструє потоковий ресурс, званий "rar", і обгортку URL, яка називається "rar wrapper", і відповідний їй префікс "rar".
