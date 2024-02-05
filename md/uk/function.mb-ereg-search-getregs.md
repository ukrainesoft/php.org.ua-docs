---
navigation:
  - function.mb-ereg-search-getpos.md: « mb\_ereg\_search\_getpos
  - function.mb-ereg-search-init.md: mb\_ereg\_search\_init »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_getregs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_getregs

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_getregs — Отримує останній збіг рядка в багатобайтовому кодуванні регулярного виразу

### Опис

```methodsynopsis
mb_ereg_search_getregs(): array|false
```

Отримує останній збіг рядка в багатобайтовому кодуванні регулярного виразу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array), що містить підрядки, що збіглися з регулярним виразом, отримані після спрацьовування функцій [mb\_ereg\_search()](function.mb-ereg-search.md) [mb\_ereg\_search\_pos()](function.mb-ereg-search-pos.md) [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.md). Якщо збігів кілька, то перший елемент міститиме співпадаючий підрядок, другий міститиме першу згруповану в дужках частину, третій елемент міститиме другу згруповану в дужках частину і так далі. Функція поверне \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg\_search\_init()](function.mb-ereg-search-init.md) \- Налаштовує рядок та регулярний вираз для пошуку відповідності рядка у багатобайтовому кодуванні регулярному виразу
