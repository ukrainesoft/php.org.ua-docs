---
navigation:
  - function.mb-ereg-search-regs.md: « mb\_ereg\_search\_regs
  - function.mb-ereg-search.md: mb\_ereg\_search »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_setpos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_setpos

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_setpos — Задає початкову позицію в рядку, з якого почнеться пошук відповідності регулярному виразу

### Опис

```methodsynopsis
mb_ereg_search_setpos(int $offset): bool
```

Функция**mb\_ereg\_search\_setpos()** задає початкову позицію, з якої почнеться пошук відповідностей регулярного вираження функцією [mb\_ereg\_search()](function.mb-ereg-search.md)

### Список параметрів

`offset`

Встановлювана позиція. Якщо передано від'ємне число, відлік триває з кінця рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.1.0 | Додано підтримку параметром `offset` негативних значень. |

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg\_search\_init()](function.mb-ereg-search-init.md) \- Налаштовує рядок та регулярний вираз для пошуку відповідності рядка у багатобайтовому кодуванні регулярному виразу
