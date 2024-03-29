---
navigation:
  - function.mb-ereg-replace-callback.md: « mb\_ereg\_replace\_callback
  - function.mb-ereg-search-getpos.md: mb\_ereg\_search\_getpos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_replace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_replace

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_replace — Замінює за регулярним виразом за допомогою багатобайтових кодувань

### Опис

```methodsynopsis
mb_ereg_replace(    string $pattern,    string $replacement,    string $string,    ?string $options = null): string|false|null
```

Сканує рядок `string`для поиска совпадений с шаблоном`pattern`, затем заменяет совпавший текст на значение параметра`replacement`

### Список параметрів

`pattern`

Шаблон регулярного виразу.

У шаблоні `pattern` можна вказувати багатобайтові символи.

`replacement`

Текст заміни.

`string`

Перевірений рядок (string).

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає результуючий рядок у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо рядок `string` неприпустима для поточного кодування, повертається значення **`null`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`options` тепер може набувати значення null. |
| 7.1.0 | Функція перевіряє, чи допустимий рядок `string` для поточного кодування. |
| 7.1.0 | Модифікатор `e` оголошено застарілим. |

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

**Увага**

Никогда не используйте модификатор`e` під час роботи з даними, отриманими з недостовірних джерел. Не виконується жодного автоматичного екранування цих даних (на відміну від [preg\_replace()](function.preg-replace.md)). Ігнорування цих вимог, швидше за все, створить вразливість виконання коду в додатку.

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_eregi\_replace()](function.mb-eregi-replace.md) \- Замінює за регулярним виразом за допомогою багатобайтових символів без урахування регістру
