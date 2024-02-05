---
navigation:
  - function.mb-ereg-search-init.md: « mb\_ereg\_search\_init
  - function.mb-ereg-search-regs.md: mb\_ereg\_search\_regs »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_search\_pos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_search\_pos

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_search\_pos — Повертає позицію і довжину збігу з регулярним виразом ділянки багатобайтового рядка

### Опис

```methodsynopsis
mb_ereg_search_pos(?string $pattern = null, ?string $options = null): array|false
```

Повертає позицію і довжину ділянки, що збіглася з регулярним виразом заздалегідь визначеного багатобайтного рядка.

Рядок для пошуку задається функцією [mb\_ereg\_search\_init()](function.mb-ereg-search-init.md)Если она не определена, будет использована строка, заданная ранее.

### Список параметрів

`pattern`

Шаблон, текст регулярного виразу.

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає масив (array), що містить два елементи. Перший елемент - зміщення в байтах, з якого починається збіг щодо початку шуканого рядка, і другий елемент - довжина збігу в байтах.

У разі виникнення помилки повертає **`false`**

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
