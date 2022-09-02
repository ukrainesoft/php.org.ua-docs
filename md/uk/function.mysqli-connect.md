---
navigation:
  - ref.mysqli.md: « Синоніми та застарілі функції Mysqli
  - function.mysqli-escape-string.md: 'mysqli::escapestring »'
  - index.md: PHP Manual
  - ref.mysqli.md: Синоніми та застарілі функції Mysqli
title: mysqliconnect
---
# mysqliconnect

(PHP 5, PHP 7, PHP 8)

mysqliconnect — Псевдонім [mysqli::construct()](mysqli.construct.md)

### Опис

Ця функція є псевдонімом: [mysqli::construct()](mysqli.construct.md)

> **Зауваження**
> 
> Якщо режим виключення mysqli вимкнено і сталася помилка з'єднання, тоді **mysqliconnect()** повертає **`false`** замість об'єкта. Для отримання помилки з'єднання можна використовувати функцію [mysqliconnecterror()](mysqli.connect-error.md)
