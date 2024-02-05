---
navigation:
  - rar.configuration.md: « Налаштування під час виконання
  - rar.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - rar.setup.md: Встановлення та налаштування
title: Типи ресурсів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Типи ресурсів

Цей модуль використовує три внутрішні ресурси: дескриптор файлу, що повертається функцією [rar\_open()](rararchive.open.md) [RarArchive](class.rararchive.md), вміст архіву, що повертається функціями [rar\_list()](rararchive.getentries.md) і [rar\_entry\_get()](rararchive.getentry.md) [RarEntry](class.rarentry.md)и тип исключений[RarException](class.rarexception.md)

Цей модуль також реєструє потоковий ресурс, званий "rar", і обгортку URL, яка називається "rar wrapper", і відповідний їй префікс "rar".
