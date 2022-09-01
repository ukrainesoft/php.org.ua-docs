---
navigation:
  - function.mb-ereg-replace.html: « mberegreplace
  - function.mb-ereg-search-getregs.html: мбeregsearchgetregs »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregsearchgetpos
---
# мбeregsearchgetpos

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchgetpos - Повертає початкову позицію наступного збігу з регулярним виразом

### Опис

```methodsynopsis
mb_ereg_search_getpos(): int
```

Повертає початкову позицію наступного збігу з регулярним виразом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**мбeregsearchgetpos()** повертає початкову позицію наступного збігу з регулярним виразом для функцій [мбeregsearch()](function.mb-ereg-search.html) [мбeregsearchpos()](function.mb-ereg-search-pos.html) [мбeregsearchregs()](function.mb-ereg-search-regs.md). Позиція представляється як числа байт з початку рядка.

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchsetpos()](function.mb-ereg-search-setpos.md) - Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу
