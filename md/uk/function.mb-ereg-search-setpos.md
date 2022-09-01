---
navigation:
  - function.mb-ereg-search-regs.html: « mberegsearchregs
  - function.mb-ereg-search.html: мбeregsearch »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregsearchsetpos
---
# мбeregsearchsetpos

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchsetpos — Задає початкову позицію в рядку, з якого почнеться пошук відповідності регулярному виразу

### Опис

```methodsynopsis
mb_ereg_search_setpos(int $offset): bool
```

**мбeregsearchsetpos()** задає початкову позицію, з якої почнеться пошук відповідностей регулярного вираження функцією [мбeregsearch()](function.mb-ereg-search.md)

### Список параметрів

`offset`

Встановлювана позиція. Якщо значення є негативним, відлік йде з кінця рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано підтримку негативних значень `offset` |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchinit()](function.mb-ereg-search-init.md) - Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного вираження
