---
navigation:
  - function.mb-ereg-replace-callback.html: « mberegreplacecallback
  - function.mb-ereg-search-getpos.html: мбeregsearchgetpos »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregreplace
---
# мбeregreplace

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregreplace — Здійснює заміну за регулярним виразом за допомогою багатобайтових кодувань

### Опис

```methodsynopsis
mb_ereg_replace(    string $pattern,    string $replacement,    string $string,    ?string $options = null): string|false|null
```

Сканує рядок `string` для пошуку збігів з `pattern`, потім замінює текст, що збігся на `replacement`

### Список параметрів

`pattern`

Шаблон регулярного виразу.

У `pattern` можуть використовуватись багатобайтові символи.

`replacement`

Текст заміни.

`string`

Перевірений рядок (string).

`options`

Опція пошуку. Детальніше дивіться [мбregexsetoptions()](function.mb-regex-set-options.md)

### Значення, що повертаються

Результуючий рядок у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо `string` некоректна для поточного кодування, повертається **`null`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `options` тепер допускає значення null. |
|  | Функція перевіряє, чи коректна `string` для поточного кодування. |
|  | Модифікатор `e` оголошено застарілим. |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

**Увага**

Ніколи не використовуйте модифікатор `e` під час роботи з даними, отриманими з недостовірних джерел. Не виконується жодного автоматичного екранування цих даних (на відміну від [pregreplace()](function.preg-replace.md)). Ігнорування цих вимог, швидше за все, створить вразливість виконання віддаленого коду у вашому додатку.

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregireplace()](function.mb-eregi-replace.md) - Здійснює заміну за регулярним виразом за допомогою багатобайтових символів без урахування регістру
