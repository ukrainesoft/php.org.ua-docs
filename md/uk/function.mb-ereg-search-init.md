---
navigation:
  - function.mb-ereg-search-getregs.md: « mb\_ereg\_search\_getregs
  - function.mb-ereg-search-pos.md: mb\_ereg\_search\_pos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_init

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_init — Налаштовує рядок та регулярний вираз для пошуку відповідності рядка в багатобайтовому кодуванні регулярного виразу

### Опис

```methodsynopsis
mb_ereg_search_init(string $string, ?string $pattern = null, ?string $options = null): bool
```

Функция**mb\_ereg\_search\_init()** задає значення параметрів `string`и`pattern` для функцій, які шукають відповідності рядків у багатобайтових кодуваннях регулярного виразу. З цими значеннями працюють функції [mb\_ereg\_search()](function.mb-ereg-search.md) [mb\_ereg\_search\_pos()](function.mb-ereg-search-pos.md) і [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.md)

### Список параметрів

`string`

Рядок пошуку.

`pattern`

Шаблон пошуку.

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметри `pattern`и`options` тепер можуть набувати значення null. |

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg\_search\_regs()](function.mb-ereg-search-regs.md) \- Повертає частину рядка, що збіглася з регулярним виразом.
