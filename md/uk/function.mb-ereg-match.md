---
navigation:
  - function.mb-encoding-aliases.md: « mb\_encoding\_aliases
  - function.mb-ereg-replace-callback.md: mb\_ereg\_replace\_callback »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_ereg\_match
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_ereg\_match

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

mb\_ereg\_match — Визначає, чи багатобайтовий рядок відповідає регулярному виразу.

### Опис

```methodsynopsis
mb_ereg_match(string $pattern, string $string, ?string $options = null): bool
```

Визначає, чи багатобайтовий рядок збігається з регулярним виразом.

> **Зауваження**: Відповідність регулярному виразу `pattern` виконуватиметься лише з початку рядка `string`

### Список параметрів

`pattern`

Шаблон регулярного виразу.

`string`

Оцінений рядок (string).

`options`

Варіант пошуку. Пояснення наведено в описі функції [mb\_regex\_set\_options()](function.mb-regex-set-options.md)

### Значення, що повертаються

Повертає **`true`**, якщо рядок `string` збігається з регулярним виразом `pattern`, иначе\*\*`false`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`options` тепер набуває значення null. |

### Примітки

> **Зауваження** :
> 
> Для цієї функції буде використано внутрішнє кодування або кодування, встановлене функцією [mb\_regex\_encoding()](function.mb-regex-encoding.md)

### Дивіться також

-   [mb\_regex\_encoding()](function.mb-regex-encoding.md) \- Встановлює/отримує кодування символів для однобайтового регулярного виразу
-   [mb\_ereg()](function.mb-ereg.md) \- Знаходить збіг регулярного виразу за допомогою багатобайтових кодувань
