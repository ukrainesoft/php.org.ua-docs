---
navigation:
  - function.mb-ereg-search-getregs.html: « mberegsearchgetregs
  - function.mb-ereg-search-pos.html: мбeregsearchpos »
  - index.html: PHP Manual
  - ref.mbstring.html: Функції для роботи з багатобайтовими рядками
title: мбeregsearchinit
---
# мбeregsearchinit

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregsearchinit — Ініціалізація пошуку відповідностей регулярному виразу багатобайтовим рядком та текстом регулярного виразу

### Опис

```methodsynopsis
mb_ereg_search_init(string $string, ?string $pattern = null, ?string $options = null): bool
```

**мбeregsearchinit()** задає значення параметрів `string` і `pattern` для функцій регулярних виразів. Ці значення будуть використовуватись у функціях [мбeregsearch()](function.mb-ereg-search.html) [мбeregsearchpos()](function.mb-ereg-search-pos.html) і [мбeregsearchregs()](function.mb-ereg-search-regs.html)

### Список параметрів

`string`

Рядок, у якому здійснюватиметься пошук відповідностей.

`pattern`

Шаблон, регулярний вираз.

`options`

Опція пошуку. Детальніше дивіться [мбregexsetoptions()](function.mb-regex-set-options.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `pattern` і `options` тепер допускають значення null. |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.html)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.html) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбeregsearchregs()](function.mb-ereg-search-regs.html) - Повертає частину рядка, що збіглася з регулярним виразом.
