---
navigation:
  - function.mb-ereg-search-pos.md: « mb\_ereg\_search\_pos
  - function.mb-ereg-search-setpos.md: mb\_ereg\_search\_setpos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_regs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_regs

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_regs — Повертає частину рядка, що збіглася з регулярним виразом.

### Опис

```methodsynopsis
mb_ereg_search_regs(?string $pattern = null, ?string $options = null): array|false
```

Повертає частину рядка, що збіглася з регулярним виразом.

### Список параметрів

`pattern`

Шаблон пошуку.

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає масив (array), у першому елементі якого буде підрядок частини, що збіглася, у другому згрупована в дужках перша частина, в третьому згрупована в дужках друга частина і так далі, якщо буде знайдено відповідність регулярному виразу рядка в багатобайтовому кодуванні. У разі виникнення помилки повертає **`false`**

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
-   [mb\_ereg\_search\_init()](function.mb-ereg-search-init.md) \- Налаштовує рядок та регулярний вираз для пошуку відповідності рядка у багатобайтовому кодуванні регулярному виразу
