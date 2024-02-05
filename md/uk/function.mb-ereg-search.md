---
navigation:
  - function.mb-ereg-search-setpos.md: « mb\_ereg\_search\_setpos
  - function.mb-ereg.md: mb\_ereg »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search — Знаходить відповідність певного рядка в багатобайтовому кодуванні регулярного виразу

### Опис

```methodsynopsis
mb_ereg_search(?string $pattern = null, ?string $options = null): bool
```

Виконує пошук відповідність визначеного рядка в багатобайтовому кодуванні регулярного виразу.

### Список параметрів

`pattern`

Шаблон пошуку.

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо багатобайтний рядок відповідає регулярному виразу, інакше **`false`**. Рядок (string) для пошуку відповідностей задається функцією [mb\_ereg\_search\_init()](function.mb-ereg-search-init.md). Якщо параметр `pattern` не заданий, буде використано попередній вираз.

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
