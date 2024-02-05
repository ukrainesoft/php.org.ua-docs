---
navigation:
  - function.mb-ereg-replace.md: « mb\_ereg\_replace
  - function.mb-ereg-search-getregs.md: mb\_ereg\_search\_getregs »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_getpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_getpos

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_getpos - Повертає початкову позицію наступного збігу з регулярним виразом

### Опис

```methodsynopsis
mb_ereg_search_getpos(): int
```

Повертає початкову позицію наступного збігу з регулярним виразом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає початкову позицію наступного збігу з регулярним виразом для функцій [mb\_ereg\_search()](function.mb-ereg-search.md) [mb\_ereg\_search\_pos()](function.mb-ereg-search-pos.md) [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.md)Позиция представлена байтами с начала строки.

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg\_search\_setpos()](function.mb-ereg-search-setpos.md) \- Задає початкову позицію у рядку, з якого розпочнеться пошук відповідностей регулярному виразу
