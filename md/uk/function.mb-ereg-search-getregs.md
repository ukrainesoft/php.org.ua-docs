---
navigation:
  - function.mb-ereg-search-getpos.html: « mberegsearchgetpos
  - function.mb-ereg-search-init.html: мбeregsearchinit »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregsearchgetregs
---
# мбeregsearchgetregs

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchgetregs - Виводить результат останнього порівняння з регулярним виразом

### Опис

```methodsynopsis
mb_ereg_search_getregs(): array|false
```

Отримання результату виконання функцій порівняння багатобайтних рядків із регулярним виразом

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) містить підрядки, що збіглися з регулярним виразом, в результаті виконання функцій [мбeregsearch()](function.mb-ereg-search.html) [мбeregsearchpos()](function.mb-ereg-search-pos.html) [мбeregsearchregs()](function.mb-ereg-search-regs.md). Якщо збігів кілька, то перший елемент міститиме співпадаючий підрядок, другий міститиме першу частину в квадратних дужках, третій елемент міститиме другу частину в квадратних дужках і так далі. Функція поверне **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchinit()](function.mb-ereg-search-init.md) - Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного виразу
