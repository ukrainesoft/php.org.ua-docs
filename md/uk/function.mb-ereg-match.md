---
navigation:
  - function.mb-encoding-aliases.md: « mbencodingaliases
  - function.mb-ereg-replace-callback.md: мбeregreplacecallback »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбeregmatch
---
# мбeregmatch

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

мбeregmatch — Збіг з регулярним виразом для багатобайтового рядка

### Опис

```methodsynopsis
mb_ereg_match(string $pattern, string $string, ?string $options = null): bool
```

Збіг з регулярним виразом для багатобайтового рядка.

> **Зауваження** `pattern` зіставляється лише на початку `string`

### Список параметрів

`pattern`

Шаблон регулярного виразу.

`string`

Оцінений рядок (string).

`options`

Опція пошуку. Детальніше дивіться [мбregexsetoptions()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає **`true`**, якщо `string` збігається з регулярним виразом `pattern` **`false`** - в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | `options` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [мбregexencoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [мбregexencoding()](function.mb-regex-encoding.md) - Встановлює/отримує поточне кодування для багатобайтового регулярного виразу
-   [мбereg()](function.mb-ereg.md) - Збіг з регулярним виразом з підтримкою багатобайтових кодувань
